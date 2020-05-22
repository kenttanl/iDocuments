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

