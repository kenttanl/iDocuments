# ETCD

- Raft：etcd 所采用的保证分布式系统强一致性的算法。
- Node：一个 Raft 状态机实例。
- Member： 一个 etcd 实例。它管理着一个 Node，并且可以为客户端请求提供服务。
- Cluster：由多个 Member 构成可以协同工作的 etcd 集群。
- Peer：对同一个 etcd 集群中另外一个 Member 的称呼。
- Client： 向 etcd 集群发送 HTTP 请求的客户端。
- WAL：预写式日志，etcd 用于持久化存储的日志格式。
- snapshot：etcd 防止 WAL 文件过多而设置的快照，存储 etcd 数据状态。
- Proxy：etcd 的一种模式，为 etcd 集群提供反向代理服务。
- Leader：Raft 算法中通过竞选而产生的处理所有数据提交的节点。
- Follower：竞选失败的节点作为 Raft 中的从属节点，为算法提供强一致性保证。
- Candidate：当 Follower 超过一定时间接收不到 Leader 的心跳时转变为 Candidate 开始竞选。
- Term：某个节点成为 Leader 到下一次竞选时间，称为一个 Term。
- Index：数据项编号。Raft 中通过 Term 和 Index 来定位数据。

# HDFS

- NameNode：负责管理文件系统的 namespace 以及客户端对文件的访问
- DataNode：用于管理它所在节点上的存储
- JournalNode：用于存储 EditLog
- FailoverController：障切换控制器，负责监控与切换 Namenode 服务
- Balancer：用于平衡集群之间各节点的磁盘利用率
- Rack：机架
- FsImage：包含自 Namenode 开始以来文件的 namespace 的完整状态
- EditLogs：包含最近对文件系统进行的与最新 FsImage 相关的所有修改
- Block：文件块
- Namespace：命名空间
- Acknowledgement：确认
- DistributedFileSystem：分布式文件系统

# HBase

- Master：主节点，负责监视集群中的所有 RegionServer 实例等
- RegionServer：负责服务和管理 regions 的节点
- LoadBalancer：负载平衡器
- CatalogJanitor：定期检查并清理 .META 表
- Split：分离
- Compact：压缩
- Minor_Compaction
- Major_compaction
- WAL：预写日志
- BlockCache：读取缓存
- MemStore：写入缓存
- Row：行
- Column Familes：列族
- Cells：单元格

# Storm

- MasterNode：控制节点
- WorkerNode：工作节点
- Nimbus：用于提交任务、分配集群任务、集群监控等 <光轮，雨云>
- Supervisor：负责接收 Nimbus 分配的任务，并管理属于自己的 Worker 进程 <监督人，管理人；监察员>
- Topology：Storm 对任务的抽象，像是一个计算节点所组成的图 <拓扑学> 
- Worker：运行具体任务处理组件逻辑的进程
- Stream：一个没有边界的 tuple 序列 <流>
- Spout：流的源头 <n. 喷口；水龙卷；水落管；水柱>
- Blot：处理输入的 Stream，并产生新的输出 Stream 的处理节点 <n. 污点，污渍；墨水渍>
- Tuple：流中基本的数据处理单元 <元组>
- ShuffleGrouping：随机分组
- FieldsGrouping：字段分组
- GlobalGrouping：全局分组
- AllGrouping：全部分组
- DirectGrouping：直接分组
- NoneGrouping：无分组
- LocalOrShuffleGrouping：本地或随机分组
- PartialKeyGrouping：部分关键字分组
