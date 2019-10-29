# 导航

- [基础系统服务（当前页面）](#基础系统服务)
- [开发工具与软件](./software.md)
- [专业名词收集](./Glossary.md)
- [Jar 包收集](./java-package.md)

# 基础系统服务

收集开发过程中，常用到的基础系统服务。它们不仅在系统的架构中承担了重要的角色，也是每个开发者都应该深入学习的优秀典范。

## Hadoop 

### 论文

:orange_book: [GFS 论文中文版](http://blog.bizcloudsoft.com/wp-content/uploads/Google-File-System%E4%B8%AD%E6%96%87%E7%89%88_1.0.pdf)  
:orange_book: [BigTable 论文中文版](http://blog.bizcloudsoft.com/wp-content/uploads/Google-Bigtable%E4%B8%AD%E6%96%87%E7%89%88_1.0.pdf)  
:orange_book: [MapReduce 论文中文版](http://blog.bizcloudsoft.com/wp-content/uploads/Google-MapReduce%E4%B8%AD%E6%96%87%E7%89%88_1.0.pdf)  

### HDFS 

- 适合运行在通用硬件上的分布式文件系统
- [官方文档，架构和设计（英文）](https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html)
- [官方文档，架构和设计（中文）](https://hadoop.apache.org/docs/r1.0.4/cn/hdfs_design.html)
- [Github 地址](https://github.com/apache/hadoop)

### HBase

- 一个分布式的、面向列的开源数据库
- [官方文档（英文）](https://hbase.apache.org/book.html#datamodel)
- [官方文档（中文）](http://abloz.com/hbase/book.html)
- [Github 地址](https://github.com/apache/hbase)

### Yarn

- Hadoop 分布式处理框架中的资源管理和作业调度技术
- [官方文档（英文）](https://hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/YARN.html)
- [Github 地址](https://github.com/apache/hadoop)

### Hive

- 基于 hadoop 的一个数据仓库工具，可以将结构化的数据文件映射为一张数据库表，并提供类SQL查询功能
- [官网文档（英文）](http://hive.apache.org)
- [Github 地址](https://github.com/apache/hive)


## Kafka

- 一个分布式流处理平台
- [官方文档（英文）](http://kafka.apache.org)
- [官方文档（中文）](http://kafka.apachecn.org)


## ELK

### Elasticsearch

- 基于Apache Lucene 的开源搜索引擎，它可以近乎实时的存储、检索数据
- [官网（中文）](https://www.elastic.co/cn/products/elasticsearch)
- [文档（英文，基于最新版本, 推荐）](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
- [文档（中文，基于 2.x 版本）](https://www.elastic.co/guide/cn/elasticsearch/guide/current/index.html)

### Kibana

- 一个开源的分析与可视化平台，用于和 Elasticsearch 一起使用
- [官网（中文）](https://www.elastic.co/cn/products/kibana/)
- [文档（中文）](https://www.elastic.co/guide/cn/kibana/current/index.html)

### Logstash

- 一个开源的数据收集引擎，具有实时管道功能
- [官网（中文）](https://www.elastic.co/cn/products/logstash)
- [文档（英文，基于最新版本）](https://www.elastic.co/guide/en/logstash/current/index.html)
- [文档（中文，基于版本不详，来源不详）](https://doc.yonyoucloud.com/doc/logstash-best-practice-cn/index.html)

## Flink

- 一个框架和分布式处理引擎，用于在无边界和有边界数据流上进行有状态的计算
- [官网（英文）](https://flink.apache.org)
- [官网（中文）](https://flink.apache.org/zh/)
- [文档（英文 v1.9）](https://ci.apache.org/projects/flink/flink-docs-release-1.9/)
- [文档（中文 v1.9）](https://ci.apache.org/projects/flink/flink-docs-release-1.9/zh/)
- [Github 地址](https://github.com/apache/flink)

## Storm

- Twitter 开源的分布式实时大数据处理框架
- [官方文档（英文）](http://storm.apache.org)
- [Github 地址](https://github.com/apache/storm)

## ETCD

- 一个分布式键值对存储，设计用来可靠而快速的保存关键数据并提供访问
- [官网（英文）](https://etcd.io)
- [文档（英文 v3.4.0）](https://etcd.io/docs/v3.4.0/)
- [文档（中文）](https://doczhcn.gitbook.io/etcd/)
- [Github 地址](https://github.com/etcd-io/etcd)

## Zookeeper

- 一个分布式的，开放源码的分布式应用程序协调服务
- [官网（英文）](https://zookeeper.apache.org)
- [文档（英文 v3.5.6）](https://zookeeper.apache.org/doc/r3.5.6/)
- [文档（中文 from w3cschool）](https://www.w3cschool.cn/zookeeper/zookeeper_overview.html)
- [Github 地址](https://github.com/apache/zookeeper)

## Redis

- 一个开源的，内存中的数据结构存储系统
- [官网（英文）](https://redis.io)
- [官网（中文）](http://www.redis.cn)
- [文档（英文）](https://redis.io/documentation)
- [文档（中文）](http://www.redis.cn/documentation.html)
- [Github 地址](https://github.com/antirez/redis)
