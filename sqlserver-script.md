### 查看正在执行的 SQL

```sql
SELECT [session_id]
    ,[request_id]
    ,[cpu_time]
    ,[start_time] AS '开始时间'
    ,[status] AS '状态'
    ,[command] AS '命令'
    ,dest.[text] AS 'SQL语句'
    ,[reads] AS '物理读次数'
    ,[writes] AS '写次数'
    ,[logical_reads] AS '逻辑读次数'
    ,[row_count] AS '返回结果行数'
    ,[blocking_session_id] AS '正在阻塞其他会话的会话ID'
    ,DB_NAME([database_id]) AS '数据库名'
    ,[wait_type] AS '等待资源类型'
    ,[wait_time] AS '等待时间'
    ,[wait_resource] AS '等待的资源'
  FROM sys.[dm_exec_requests] AS der
  CROSS APPLY sys.[dm_exec_sql_text](der.[sql_handle]) AS dest
  WHERE 1=1
  ORDER BY [cpu_time] DESC
```

### 查看当前死锁

```sql
SELECT request_session_id AS spid
    ,OBJECT_NAME(resource_associated_entity_id) AS tableName
  FROM sys.dm_tran_locks
  WHERE resource_type = 'OBJECT'
```

### 查看进程信息

```sql
SELECT spid
    ,blocked
    ,DB_NAME(sp.dbid) AS DBName
    ,program_name
    ,waitresource
    ,lastwaittype
    ,sp.loginame
    ,sp.hostname
    ,a.[Text] AS [TextData]
    ,SUBSTRING(A.TEXT, sp.stmt_start / 2, 
        (CASE WHEN sp.stmt_end = -1 
              THEN DATALENGTH(A.TEXT) 
              ELSE sp.stmt_end END - sp.stmt_start) / 2) AS [current_cmd]
  FROM sys.sysprocesses sp
    OUTER APPLY sys.dm_exec_sql_text(sp.sql_handle) A
  WHERE spid IN (
          SELECT blocked
            FROM sys.sysprocesses
           WHERE blocked > 0)
        OR blocked != 0
  ORDER BY blocked DESC, spid ASC, DB_NAME(sp.dbid) ASC, a.[text]
  ```
  
### 查看服务器时区
  
```sql
DECLARE @TimeZone NVARCHAR(255)
EXEC master.dbo.xp_instance_regread
	N'HKEY_LOCAL_MACHINE',
	N'SYSTEM\CurrentControlSet\Control\TimeZoneInformation',
	N'TimeZoneKeyName',
	@TimeZone 
OUTPUT SELECT @TimeZone
```

### 查询表字段类型定义

注：使用 object_id 函数能够避免 table_name 格式化问题

```sql
SELECT table_catalog AS database_name
     ,table_schema AS schema_name
     ,table_name
     ,column_name
     ,data_type
     ,character_maximum_length
     ,tc.* 
 FROM information_schema.columns tc
WHERE EXISTS (
    SELECT 1 FROM sys.objects obj 
     WHERE obj.object_id=object_id('my_table')
       AND obj.name=tc.table_name 
       AND tc.table_schema=SCHEMA_NAME(obj.schema_id)
 )
```

### 查询 CPU 和内存信息

Outlink: [Monitor CPU and Memory usage for all SQL Server instances using PowerShell](https://www.mssqltips.com/sqlservertip/5724/monitor-cpu-and-memory-usage-for-all-sql-server-instances-using-powershell/)

```sql
WITH SQLProcessCPU
AS(
   SELECT TOP(30) SQLProcessUtilization AS 'CPU_Usage', ROW_NUMBER() OVER(ORDER BY (SELECT NULL)) AS 'row_number'
   FROM ( 
         SELECT 
           record.value('(./Record/@id)[1]', 'int') AS record_id,
           record.value('(./Record/SchedulerMonitorEvent/SystemHealth/SystemIdle)[1]', 'int') AS [SystemIdle],
           record.value('(./Record/SchedulerMonitorEvent/SystemHealth/ProcessUtilization)[1]', 'int') AS [SQLProcessUtilization], 
           [timestamp] 
         FROM ( 
              SELECT [timestamp], CONVERT(xml, record) AS [record] 
              FROM sys.dm_os_ring_buffers 
              WHERE ring_buffer_type = N'RING_BUFFER_SCHEDULER_MONITOR' 
              AND record LIKE '%<SystemHealth>%'
              ) AS x 
        ) AS y
) 

SELECT 
   SERVERPROPERTY('SERVERNAME') AS 'Instance',
   (SELECT value_in_use FROM sys.configurations WHERE name like '%max server memory%') AS 'Max Server Memory',
   (SELECT physical_memory_in_use_kb/1024 FROM sys.dm_os_process_memory) AS 'SQL Server Memory Usage (MB)',
   (SELECT total_physical_memory_kb/1024 FROM sys.dm_os_sys_memory) AS 'Physical Memory (MB)',
   (SELECT available_physical_memory_kb/1024 FROM sys.dm_os_sys_memory) AS 'Available Memory (MB)',
   (SELECT system_memory_state_desc FROM sys.dm_os_sys_memory) AS 'System Memory State',
   (SELECT [cntr_value] FROM sys.dm_os_performance_counters WHERE [object_name] LIKE '%Manager%' AND [counter_name] = 'Page life expectancy') AS 'Page Life Expectancy',
   (SELECT AVG(CPU_Usage) FROM SQLProcessCPU WHERE row_number BETWEEN 1 AND 30) AS 'SQLProcessUtilization30',
   (SELECT AVG(CPU_Usage) FROM SQLProcessCPU WHERE row_number BETWEEN 1 AND 15) AS 'SQLProcessUtilization15',
   (SELECT AVG(CPU_Usage) FROM SQLProcessCPU WHERE row_number BETWEEN 1 AND 10) AS 'SQLProcessUtilization10',
   (SELECT AVG(CPU_Usage) FROM SQLProcessCPU WHERE row_number BETWEEN 1 AND 5)  AS 'SQLProcessUtilization5',
   GETDATE() AS 'Data Sample Timestamp'
```

**说明：**

- **Instance:** SQL Server实例的名称
- **Max Server Memory:** SQL Server 进程最多使用多少内存
- **SQL Server Memory Usage (MB):** SQL Server 进程正在使用多少内存
- **Physical Memory (MB):** 操作系统最多可以使用多少内存
- **Available Memory (MB):** 服务器上可以使用的剩余内存
- **System Memory State:** 根据使用情况/可用性，简要描述内存状态
- **Page Life Expectancy:** 数据采样时为PLE
- **SQLProcessUtilization30, SQLProcessUtilization15, SQLProcessUtilization10 and SQLProcessUtilization5:** 过去 30/15/10/5 分钟的平均 CPU 使用率
- **Data Sample Timestamp:** 捕获数据时的服务器时间


### 开启数据库与表的 CT

```sql
-- 开启数据库的 CT
ALTER DATABASE [Database_Name]
SET CHANGE_TRACKING = ON 
(CHANGE_RETENTION = 3 DAYS, AUTO_CLEANUP = ON)

-- 开启表的 CT
ALTER TABLE [dbo].[Table_Name]  
ENABLE CHANGE_TRACKING  
WITH (TRACK_COLUMNS_UPDATED = ON)  
```

### 关闭数据库与表的 CT

```sql
-- 关闭数据库的 CT
ALTER DATABASE [Database_Name]
SET CHANGE_TRACKING = OFF  

-- 关闭表的 CT
ALTER TABLE [dbo].[Table_Name]  
DISABLE CHANGE_TRACKING;  
```

### 查询 CT 表数据

Outlink: [使用更改跟踪 (SQL Server)](https://docs.microsoft.com/zh-cn/sql/relational-databases/track-changes/work-with-change-tracking-sql-server?view=sql-server-ver15)

```sql
declare @last_synchronization_version bigint;

SELECT  
    CT.ID, CT.SYS_CHANGE_OPERATION,  
    CT.SYS_CHANGE_COLUMNS, CT.SYS_CHANGE_CONTEXT  
FROM  
    CHANGETABLE(CHANGES [dbo].[Table_Name], @last_synchronization_version) AS CT
```

