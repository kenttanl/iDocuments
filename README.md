### 分类导航

[Hadoop](#hadoop)、[消息队列服务](#消息队列服务)、[ELK](#elk)、[流计算](#流计算)、[服务发现与配置](#服务发现与配置)、[NoSQL/RDBMS](#nosqlrdbms)、[监控与显示](#监控与显示)、[Web 服务器/代理](#web-服务器--代理)、[容器](#容器)、[CI/CD/质量管理](#cicd质量管理)、[对象存储](#对象存储)、[API 网关](#api-网关)、[任务调度](#任务调度)、[安全与认证](#安全与认证)、[基础原理可视化](#基础原理可视化)

# 基础系统服务

收集开发过程中，常用到的基础系统服务。它们不仅在系统的架构中承担了重要的角色，也是每个开发者都应该深入学习的优秀典范。点击下面的 logo 可直接跳转到对应条目。

[<img height="50" src="./imgs/hadoop-logo.png" alt="Hadoop" title="Hadoop: 一个由 Apache 基金会所开发的分布式系统基础架构" />](#hadoop)
[<img height="50" src="./imgs/hdfs-logo.png" alt="HDFS" title="HDFS: 适合运行在通用硬件上的分布式文件系统" />](#hdfs)
[<img height="50" src="./imgs/hbase-logo.png" alt="HBase" title="HBase: 一个分布式的、面向列的开源数据库" />](#hbase)
[<img height="50" src="./imgs/hive-logo.png" alt="Hive" title="Hive: 基于 hadoop 的一个数据仓库工具，可以将结构化的数据文件映射为一张数据库表，并提供类SQL查询功能" />](#hive)
[<img height="50" src="./imgs/kylin-logo.png" alt="Kylin" title="Kylin: 一个开源的、分布式的分析型数据仓库，提供 Hadoop 之上的 SQL 查询接口及多维分析（OLAP）能力以支持超大规模数据" />](#kylin)
[<img height="40" width="140" src="./imgs/parquet-logo.png" alt="Parquet" title="Parquet: 一种高效的列式存储格式，适用于 Hadoop 生态系统中的任何项目，被广泛应用于数据分析、数据湖、机器学习、数据仓库等领域" />](#parquet)
[<img height="50" src="./imgs/spark-logo.png" alt="Spark" title="Spark: 一个快速的，用于海量数据处理的通用引擎" />](#spark)
[<img height="50" src="./imgs/iceberg-logo.svg" alt="Apache Iceberg" title="Apache Iceberg: 专为超大规模分析数据集设计的开放表格式，支持 ACID 事务和 Schema 演化" />](#apache-iceberg)
[<img height="50" src="./imgs/apache-paimon-logo.png" alt="Apache Paimon" title="Apache Paimon: 支持实时湖仓一体架构的流式数据湖存储格式，由 Flink 社区孵化" />](#apache-paimon)
[<img height="50" src="./imgs/doris-logo.svg" alt="Apache Doris" title="Apache Doris: 高性能实时 MPP 分析型数据库，兼容 MySQL 协议，支持秒级 Ad-hoc 可以查询" />](#apache-doris)
[<img height="50" src="./imgs/kafka-logo.png" alt="Kafka" title="Kafka: 一个分布式流处理平台，目标是为处理实时数据提供一个统一、高吞吐、低延迟的平台" />](#kafka)
[<img height="50" src="./imgs/activemq-logo.png" alt="ActiveMQ" title="ActiveMQ: 一个多协议、基于Java的消息传递服务器" />](#activemq)
[<img height="50" src="./imgs/rocketmq-logo.png" alt="RocketMQ" title="RocketMQ: 阿里巴巴在 2012 年开源的分布式消息中间件" />](#rocketmq)
[<img height="40" src="./imgs/rabbitmq-logo.svg" alt="RabbitMQ" title="RabbitMQ: 可以为你的应用提供一个通用的消息发送和接收平台，并且保证消息在传输过程中的安全" />](#rabbitmq)
[<img height="40" src="./imgs/zeromq-logo.svg" alt="ZeroMQ" title="ZeroMQ: An open-source universal messaging library" />](#zeromq)
[<img height="50" src="./imgs/pulsar-logo.svg" alt="Apache Pulsar" title="Apache Pulsar: 云原生分布式消息流平台，支持多租户、持久化存储与计算存储分离" />](#apache-pulsar)
[<img height="50" src="./imgs/nats-logo.svg" alt="NATS" title="NATS: 超轻量高性能云原生消息系统，延迟极低，适合微服务与边缘计算" />](#nats)
[<img height="50" src="./imgs/elasticsearch-logo.png" alt="Elasticsearch" title="Elasticsearch: 基于Apache Lucene 的开源搜索引擎，它可以近乎实时的存储、检索数据" />](#elasticsearch)
[<img height="50" src="./imgs/kibana-logo.png" alt="Kibana" title="Kibana:  一个开源的分析与可视化平台，用于和 Elasticsearch 一起使用" />](#kibana)
[<img height="50" src="./imgs/logstash-logo.png" alt="Logstash" title="Logstash: 一个开源的数据收集引擎，具有实时管道功能" />](#logstash)
[<img height="50" src="./imgs/filebeat-logo.jpg" alt="Filebeat" title="Filebeat: 轻量型日志采集器（基于 Go 语言开发）" />](#filebeat)
[<img height="50" src="./imgs/loki-logo.png" alt="Loki" title="Loki: Grafana 出品的轻量级日志聚合系统，仅索引标签元数据，成本极低" />](#loki)
[<img height="50" src="./imgs/flink-logo.svg" alt="Flink" title="Flink: 一个框架和分布式处理引擎，用于在无边界和有边界数据流上进行有状态的计算" />](#flink)
[<img height="50" src="./imgs/storm-logo.png" alt="Storm" title="Storm: Twitter 开源的分布式实时大数据处理框架" />](#storm)
[<img height="50" src="./imgs/etcd-logo.png" alt="ETCD" title="ETCD: 一个分布式键值对存储，设计用来可靠而快速的保存关键数据并提供访问" />](#etcd)
[<img height="50" src="./imgs/zookeeper-logo.png" alt="Zookeeper" title="Zookeeper: 一个分布式的、开放源码的分布式应用程序协调服务" />](#zookeeper)
[<img height="50" src="./imgs/consul-logo.png" alt="Consul" title="Consul: 一种服务网格解决方案，提供具有服务发现，配置和分段功能的全功能控制平面" />](#consul)
[<img height="40" width="170" src="./imgs/nacos-logo.png" alt="Nacos" title="Nacos: 致力于帮助您发现、配置和管理微服务；帮助您更敏捷和容易地构建、交付和管理微服务平台" />](#nacos)
[<img height="50" src="./imgs/apollo-logo.png" alt="Apollo" title="Apollo: 携程开源的分布式配置中心，支持多环境、多集群、灰度发布和权限管理" />](#apollo)
[<img height="50" src="./imgs/redis-logo.png" alt="Redis" title="Redis: 一个开源的，内存中的数据结构存储系统" />](#redis)
[<img height="50" src="./imgs/mongodb-logo.png" alt="MongoDB" title="MongoDB: 一个通用的、基于分布式文件存储的数据库" />](#mongodb)
[<img height="50" src="./imgs/cassandra-logo.png" alt="Cassandra" title="Cassandra: 一个高度可扩展的分区行存储系统" />](#cassandra)
[<img height="50" src="./imgs/memcached-logo.png" alt="Memcached" title="Memcached: 一个高性能的、分布式内存对象缓存系统" />](#memcached)
[<img height="50" src="./imgs/evcache-logo.png" alt="EVCache" title="EVCache: ​​基于 memcached 和 spymemcached 的缓存解决方案，主要用于 AWS EC2 基础设施来缓存常用数据" />](#evcache)
[<img height="50" src="./imgs/aerospike-logo.png" alt="Aerospike" title="Aerospike: ​​第一个 NoSQL 数据库，为始终在线的全球分布式业务交易，在大规模和一致性之间找到了平衡" />](#aerospike)
[<img height="50" src="./imgs/clickhouse-logo.png" alt="ClickHouse" title="ClickHouse: 一个开源的、面向列的 OLAP 数据库管理系统，可以实时生成数据分析报告" />](#clickHouse)
[<img height="50" src="./imgs/opentsdb-logo.png" alt="OpenTSDB" title="OpenTSDB: 在不丢失粒度的情况下存储和提供大量时间序列数据" />](#opentsdb)
[<img height="50" src="./imgs/druid-logo.png" alt="ApacheDruid" title="ApacheDruid: ​一个高性能的实时分析数据库，可在大规模的负载下对流式传输和批处理数据提供亚秒级查询" />](#apachedruid)
[<img height="50" src="./imgs/tidb-logo.png" alt="TiDB" title="TiDB: 开源分布式 HTAP 数据库，兼容 MySQL 协议，支持水平弹性扩展" />](#tidb)
[<img height="50" src="./imgs/neo4j-logo.svg" alt="Neo4j" title="Neo4j: 开源原生图数据库，适合社交网络、知识图谱等复杂关系数据分析" />](#neo4j)
[<img height="50" src="./imgs/prometheus-logo.png" alt="Prometheus" title="Prometheus: 一个开源的监控报警系统和时序列数据库（TSDB）" />](#prometheus)
[<img height="50" src="./imgs/grafana-logo.svg" alt="Grafana" title="Grafana: 一个开源的度量分析和可视化工具，可以通过将采集的数据查询然后可视化的展示，并及时通知" />](#grafana)
[<img height="50" src="./imgs/skywalking-logo.svg" alt="Apache SkyWalking" title="Apache SkyWalking: 分布式系统应用性能监控工具，支持 Tracing、Metrics、Logging 三位一体" />](#apache-skywalking)
[<img height="50" src="./imgs/jaeger-logo.png" alt="Jaeger" title="Jaeger: Uber 开源的端到端分布式链路追踪系统，已捐赠 CNCF" />](#jaeger)
[<img height="50" src="./imgs/opentelemetry-logo.svg" alt="OpenTelemetry" title="OpenTelemetry: CNCF 云原生可观测性标准框架，统一 Metrics、Logs、Traces 采集规范" />](#opentelemetry)
[<img height="50" src="./imgs/nginx-logo.png" alt="Nginx" title="Nginx: 一个免费的，开源的高性能 HTTP 服务器和反向代理，以及 IMAP/POP3 代理服务器" />](#nginx)
[<img height="50" src="./imgs/openresty-logo.png" alt="OpenResty" title="OpenResty: 一款基于 NGINX 和 LuaJIT 的 Web 平台" />](#openresty)
[<img height="50" src="./imgs/apache-httpd-logo.png" alt="Apache httpd" title="Apache httpd: 世界使用排名第一的 Web 服务器软件，它可以运行在几乎所有广泛使用的计算机平台上" />](#apache_httpd)
[<img height="50" src="./imgs/haproxy-logo.png" alt="HAProxy" title="HAProxy: HAProxy 是一款免费的，可为基于 TCP 和 HTTP 的应用程序提供高可用、负载均衡和代理的非常快速且可靠的解决方案。它特别适合于流量非常高的网站，并为世界上许多访问量最大的网站提供支持" />](#haproxy)
[<img height="50" src="./imgs/tengine-logo.png" alt="Tengine" title="Tengine: 由淘宝网发起的 Web 服务器项目。它在 Nginx 的基础上，针对大访问量网站的需求，添加了很多高级功能和特性。Tengine 的性能和稳定性已经在大型的网站如淘宝网、天猫商城等得到了很好的检验。它的最终目标是打造一个高效、稳定、安全、易用的 Web 平台" />](#tengine)
[<img height="50" src="./imgs/lvs-logo.gif" alt="LVS" title="LVS: 具有某些高级功能的 Linux 虚拟服务器发行版。它引入了一种新的数据包转发方法 FULLNAT，以及针对 Synflooding 攻击的防御机制 - SYNPROXY" />](#lvs)
[<img height="50" src="./imgs/keepalived-logo.png" alt="Keepalived" title="Keepalived: 基于 VRRP 协议，为 Linux 系统和基于 Linux 的基础架构提供负载均衡和高可用性的简单而强大的功能" />](#keepalived)
[<img height="50" src="./imgs/docker-logo.png" alt="Docker" title="Docker: 一个开源的应用容器引擎，让开发者可以打包他们的应用以及依赖包到一个可移植的镜像中，然后发布到任何流行的 Linux 或 Windows 机器上" />](#docker)
[<img height="50" src="./imgs/kubernetes-logo.png" alt="Kubernetes" title="Kubernetes: 一个可移植的、可扩展的开源平台，用于管理容器化的工作负载和服务，可促进声明式配置和自动化" />](#kubernetes)
[<img height="50" src="./imgs/kubesphere-logo.png" alt="Kubesphere" title="Kubesphere: 面向云原生应用的容器混合云，愿景是打造一个以 Kubernetes 为内核的云原生分布式操作系统" />](#kubesphere)
[<img height="50" src="./imgs/helm-logo.svg" alt="Helm" title="Helm: Kubernetes 应用包管理器，通过 Chart 模板标准化应用部署" />](#helm)
[<img height="50" src="./imgs/istio-logo.png" alt="Istio" title="Istio: CNCF 开源服务网格，提供流量管理、安全通信与可观测能力" />](#istio)
[<img height="50" src="./imgs/harbor-logo.png" alt="Harbor" title="Harbor: CNCF 毕业的开源企业级容器镜像仓库，支持镜像安全扫描与访问控制" />](#harbor)
[<img height="50" src="./imgs/argocd-logo.png" alt="Argo CD" title="Argo CD: 基于 GitOps 的 Kubernetes 声明式持续交付工具，Git 仓库即真相" />](#argo-cd)
[<img height="50" src="./imgs/jenkins-logo.png" alt="Jenkins" title="Jenkins: 一个提供友好操作界面的持续集成工具" />](#jenkins)
[<img height="50" src="./imgs/sonarqube-logo.svg" alt="SonarQube" title="SonarQube: 一个用于代码质量管理的开放平台" />](#sonarqube)
[<img height="50" src="./imgs/spinnaker-logo.svg" alt="Spinnaker " title="Spinnaker : 一个开源的持续交付平台，用于快速、可靠地发布软件更改" />](#spinnaker)
[<img height="50" src="./imgs/serenitybdd-logo.png" alt="Serenity BDD" title="Serenity BDD : 一个测试自动化库，旨在简化编写自动验收测试的过程，并使其更加有趣" />](#serenitybdd)
[<img height="50" src="./imgs/minio-logo.png" alt="MinIO" title="MinIO: 高性能 S3 兼容对象存储，适用于 AI/ML 数据湖场景，单体或分布式部署均可" />](#minio)
[<img height="50" src="./imgs/apisix-logo.svg" alt="Apache APISIX" title="Apache APISIX: 云原生高性能 API 网关，支持动态路由、插件热加载与 gRPC/WebSocket" />](#apache-apisix)
[<img height="50" src="./imgs/kong-logo.svg" alt="Kong" title="Kong: 云原生 API 网关与服务连接平台，插件生态丰富，支持 Kubernetes Ingress" />](#kong)
[<img height="50" src="./imgs/traefik-logo.png" alt="Traefik" title="Traefik: 云原生应用代理，支持自动服务发现与动态配置，零重启热更新" />](#traefik)
[<img height="50" src="./imgs/xxl-job-logo.jpg" alt="XXL-JOB" title="XXL-JOB: 轻量级分布式任务调度平台，开箱即用，国内使用广泛" />](#xxl-job)
[<img height="50" src="./imgs/dolphinscheduler-logo.png" alt="Apache DolphinScheduler" title="Apache DolphinScheduler: 云原生分布式可视化工作流调度平台，支持 DAG 依赖编排" />](#apache-dolphinscheduler)
[<img height="50" src="./imgs/keycloak-logo.svg" alt="Keycloak" title="Keycloak: 开源身份认证与访问管理系统，支持 SSO、OAuth2、OIDC 和 SAML" />](#keycloak)
[<img height="50" src="./imgs/vault-logo.svg" alt="HashiCorp Vault" title="HashiCorp Vault: 基于身份的密钥与敏感数据安全管理工具，支持动态凭证与加密即服务" />](#hashicorp-vault)

## Hadoop 

### 论文

:orange_book: [GFS 论文中文版](./docs/Google-File-System中文版_1.0.pdf)，[外网链接](http://blog.bizcloudsoft.com/wp-content/uploads/Google-File-System%E4%B8%AD%E6%96%87%E7%89%88_1.0.pdf)  
:orange_book: [BigTable 论文中文版](./docs/Google-Bigtable中文版_1.0.pdf)，[外网链接](http://blog.bizcloudsoft.com/wp-content/uploads/Google-Bigtable%E4%B8%AD%E6%96%87%E7%89%88_1.0.pdf)  
:orange_book: [MapReduce 论文中文版](./docs/Google-MapReduce中文版_1.0.pdf)，[外网链接](http://blog.bizcloudsoft.com/wp-content/uploads/Google-MapReduce%E4%B8%AD%E6%96%87%E7%89%88_1.0.pdf)  

### HDFS 

- [ ] 适合运行在通用硬件上的分布式文件系统
- [ ] [官方文档，架构和设计（英文）](https://hadoop.apache.org/docs/r1.2.1/hdfs_design.html)
- [ ] [官方文档，架构和设计（中文）](https://hadoop.apache.org/docs/r1.0.4/cn/hdfs_design.html)
- [ ] [Github 地址](https://github.com/apache/hadoop) <sub> [![Star](https://img.shields.io/github/stars/apache/hadoop?style=social&label=Star)](https://github.com/apache/hadoop) </sub>

### HBase 

- [ ] 一个分布式的、面向列的开源数据库
- [ ] [官方文档（英文）](https://hbase.apache.org/book.html#datamodel)
- [ ] [官方文档（中文）](http://abloz.com/hbase/book.html)
- [ ] [Github 地址](https://github.com/apache/hbase) <sub> [![Star](https://img.shields.io/github/stars/apache/hbase?style=social&label=Star)](https://github.com/apache/hbase) </sub>

### Yarn

- [ ] Hadoop 分布式处理框架中的资源管理和作业调度技术
- [ ] [官方文档（英文）](https://hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/YARN.html)
- [ ] [Github 地址](https://github.com/apache/hadoop) <sub> [![Star](https://img.shields.io/github/stars/apache/hadoop?style=social&label=Star)](https://github.com/apache/hadoop) </sub>

### Hive

- [ ] 基于 hadoop 的一个数据仓库工具，可以将结构化的数据文件映射为一张数据库表，并提供类SQL查询功能
- [ ] [官网文档（英文）](http://hive.apache.org)
- [ ] [Github 地址](https://github.com/apache/hive) <sub> [![Star](https://img.shields.io/github/stars/apache/hive?style=social&label=Star)](https://github.com/apache/hive) </sub>

### Kylin

- [ ] 一个开源的、分布式的分析型数据仓库，提供 Hadoop 之上的 SQL 查询接口及多维分析（OLAP）能力以支持超大规模数据
- [ ] [官网（英文）](https://kylin.apache.org/)
- [ ] [官网（中文）](https://kylin.apache.org/cn/)
- [ ] [官网文档（英文）](https://kylin.apache.org/docs/)
- [ ] [官网文档（中文）](https://kylin.apache.org/cn/docs/)
- [ ] [Github 地址](https://github.com/apache/kylin) <sub> [![Star](https://img.shields.io/github/stars/apache/kylin?style=social&label=Star)](https://github.com/apache/kylin) </sub>

### Parquet

- [ ] 一种高效的列式存储格式，适用于 Hadoop 生态系统中的任何项目，被广泛应用于数据分析、数据湖、机器学习、数据仓库等领域
- [ ] [官网（英文）](https://parquet.apache.org/)
- [ ] [官网文档（英文）](https://parquet.apache.org/docs/)
- [ ] [Github 地址](https://github.com/apache/parquet-mr/) <sub> [![Star](https://img.shields.io/github/stars/apache/parquet-mr?style=social&label=Star)](https://github.com/apache/parquet-mr/) </sub>

### Apache Iceberg

- [ ] 专为超大规模分析数据集设计的开放表格式，支持 ACID 事务、Schema 演化与时间旅行查询
- [ ] [官网（英文）](https://iceberg.apache.org/)
- [ ] [官方文档（英文）](https://iceberg.apache.org/docs/latest/)
- [ ] [Github 地址](https://github.com/apache/iceberg) <sub> [![Star](https://img.shields.io/github/stars/apache/iceberg?style=social&label=Star)](https://github.com/apache/iceberg) </sub>

### Apache Paimon

- [ ] 支持实时湖仓一体架构的流式数据湖存储格式，由 Flink 社区孵化，兼容 Flink、Spark、Hive
- [ ] [官网（英文）](https://paimon.apache.org/)
- [ ] [官方文档（英文）](https://paimon.apache.org/docs/stable/)
- [ ] [Github 地址](https://github.com/apache/paimon) <sub> [![Star](https://img.shields.io/github/stars/apache/paimon?style=social&label=Star)](https://github.com/apache/paimon) </sub>

### Apache Doris

- [ ] 高性能实时 MPP 分析型数据库，兼容 MySQL 协议，支持秒级 Ad-hoc 查询与高并发点查
- [ ] [官网（英文）](https://doris.apache.org/)
- [ ] [官网（中文）](https://doris.apache.org/zh-CN/)
- [ ] [官方文档（英文）](https://doris.apache.org/docs/get-starting/what-is-apache-doris)
- [ ] [官方文档（中文）](https://doris.apache.org/zh-CN/docs/get-starting/what-is-apache-doris)
- [ ] [Github 地址](https://github.com/apache/doris) <sub> [![Star](https://img.shields.io/github/stars/apache/doris?style=social&label=Star)](https://github.com/apache/doris) </sub>

## Spark

- [ ] 一个快速的，用于海量数据处理的通用引擎
- [ ] [官网（英文）](https://spark.apache.org/)
- [ ] [官网文档（英文）](https://spark.apache.org/docs/latest/)
- [ ] [翻译文档（中文）](https://spark.apachecn.org/#/)
- [ ] [Github 地址](https://github.com/apache/spark) <sub> [![Star](https://img.shields.io/github/stars/apache/spark?style=social&label=Star)](https://github.com/apache/spark) </sub>

## 消息队列服务

### Kafka 

- [ ] 一个分布式流处理平台，目标是为处理实时数据提供一个统一、高吞吐、低延迟的平台
- [ ] [官方文档（英文）](http://kafka.apache.org)
- [ ] [官方文档（中文）](http://kafka.apachecn.org)
- [ ] [Confluence（英文）](https://cwiki.apache.org/confluence/display/KAFKA/Index)
- [ ] [Github 地址](https://github.com/apache/kafka) <sub> [![Star](https://img.shields.io/github/stars/apache/kafka?style=social&label=Star)](https://github.com/apache/kafka) </sub>
- [ ] [Kafka Tool](https://www.kafkatool.com/)：用于管理和使用 Kafka 集群的 GUI 应用程序，可以快速查看 Kafka 集群中的对象以及存储在 Topic 中的消息

### ActiveMQ 

- [ ] 一个多协议、基于 Java 的消息传递服务器
- [ ] [官网（英文）](http://activemq.apache.org)
- [ ] [官方文档（英文）](http://activemq.apache.org/getting-started.html)
- [ ] [Github 地址](https://github.com/apache/activemq) <sub> [![Star](https://img.shields.io/github/stars/apache/activemq?style=social&label=Star)](https://github.com/apache/activemq) </sub>

### RocketMQ 

- [ ] 阿里巴巴在 2012 年开源的分布式消息中间件
- [ ] [官网（英文）](http://rocketmq.apache.org)
- [ ] [官方文档（英文）](http://rocketmq.apache.org/docs/quick-start/)
- [ ] [Github 地址](https://github.com/apache/rocketmq/) <sub> [![Star](https://img.shields.io/github/stars/apache/rocketmq?style=social&label=Star)](https://github.com/apache/rocketmq/) </sub>

### RabbitMQ 

- [ ] 可以为你的应用提供一个通用的消息发送和接收平台，并且保证消息在传输过程中的安全
- [ ] [官网（英文）](https://www.rabbitmq.com)
- [ ] [官方文档（英文）](https://www.rabbitmq.com/documentation.html)
- [ ] [翻译文档（中文）](http://rabbitmq.mr-ping.com)
- [ ] [Github 地址](https://github.com/rabbitmq)

### ZeroMQ 

- [ ] An open-source universal messaging library
- [ ] [官网（英文）](https://zeromq.org)
- [ ] [官方文档（英文）](https://zeromq.org/get-started/)
- [ ] [Github 地址](https://github.com/zeromq)

### Apache Pulsar

- [ ] 云原生分布式消息流平台，支持多租户、持久化存储与计算存储分离，原生支持 Geo-Replication
- [ ] [官网（英文）](https://pulsar.apache.org/)
- [ ] [官网（中文）](https://pulsar.apache.org/zh-CN/)
- [ ] [官方文档（英文）](https://pulsar.apache.org/docs/)
- [ ] [Github 地址](https://github.com/apache/pulsar) <sub> [![Star](https://img.shields.io/github/stars/apache/pulsar?style=social&label=Star)](https://github.com/apache/pulsar) </sub>

### NATS

- [ ] 超轻量高性能云原生消息系统，延迟极低，适合微服务、IoT 与边缘计算场景
- [ ] [官网（英文）](https://nats.io/)
- [ ] [官方文档（英文）](https://docs.nats.io/)
- [ ] [Github 地址](https://github.com/nats-io/nats-server) <sub> [![Star](https://img.shields.io/github/stars/nats-io/nats-server?style=social&label=Star)](https://github.com/nats-io/nats-server) </sub>

## ELK

### Elasticsearch

- [ ] 基于Apache Lucene 的开源搜索引擎，它可以近乎实时的存储、检索数据
- [ ] [官网（中文）](https://www.elastic.co/cn/products/elasticsearch)
- [ ] [官方文档（英文，基于最新版本, 推荐）](https://www.elastic.co/guide/en/elasticsearch/reference/current/index.html)
- [ ] [官方文档（中文，基于 2.x 版本）](https://www.elastic.co/guide/cn/elasticsearch/guide/current/index.html)

### Kibana

- [ ] 一个开源的分析与可视化平台，用于和 Elasticsearch 一起使用
- [ ] [官网（中文）](https://www.elastic.co/cn/products/kibana/)
- [ ] [官方文档（中文）](https://www.elastic.co/guide/cn/kibana/current/index.html)

### Logstash

- [ ] 一个开源的数据收集引擎，具有实时管道功能
- [ ] [官网（中文）](https://www.elastic.co/cn/products/logstash)
- [ ] [官方文档（英文，基于最新版本）](https://www.elastic.co/guide/en/logstash/current/index.html)
- [ ] [翻译文档（中文，基于版本不详，来源不详）](https://doc.yonyoucloud.com/doc/logstash-best-practice-cn/index.html)

### Filebeat

- [ ] 轻量型日志采集器（基于 Go 语言开发）
- [ ] [官网（中文）](https://www.elastic.co/cn/beats/filebeat)
- [ ] [官方文档（英文，基于最新版本）](https://www.elastic.co/guide/en/beats/filebeat/current/index.html)
- [ ] [翻译文档（中文，基于版本不详，来源不详）](https://elkguide.elasticsearch.cn/beats/file.html)

### Loki

- [ ] Grafana 出品的轻量级日志聚合系统，仅索引标签元数据而非全文，成本极低，与 Prometheus 生态深度集成
- [ ] [官网（英文）](https://grafana.com/oss/loki/)
- [ ] [官方文档（英文）](https://grafana.com/docs/loki/latest/)
- [ ] [Github 地址](https://github.com/grafana/loki) <sub> [![Star](https://img.shields.io/github/stars/grafana/loki?style=social&label=Star)](https://github.com/grafana/loki) </sub>

## 流计算

### Flink

- [ ] 一个框架和分布式处理引擎，用于在无边界和有边界数据流上进行有状态的计算
- [ ] [官网（英文）](https://flink.apache.org)
- [ ] [官网（中文）](https://flink.apache.org/zh/)
- [ ] [官方文档（英文 v1.9）](https://ci.apache.org/projects/flink/flink-docs-release-1.9/)
- [ ] [官方文档（中文 v1.9）](https://ci.apache.org/projects/flink/flink-docs-release-1.9/zh/)
- [ ] [Github 地址](https://github.com/apache/flink) <sub> [![Star](https://img.shields.io/github/stars/apache/flink?style=social&label=Star)](https://github.com/apache/flink) </sub>

### Storm

- [ ] Twitter 开源的分布式实时大数据处理框架
- [ ] [官方文档（英文）](http://storm.apache.org)
- [ ] [Github 地址](https://github.com/apache/storm) <sub> ![Star](https://img.shields.io/github/stars/apache/storm?style=social&label=Star) </sub>

## 服务发现与配置

### ETCD

- [ ] 一个分布式键值对存储，设计用来可靠而快速的保存关键数据并提供访问
- [ ] [官网（英文）](https://etcd.io)
- [ ] [官方文档（英文 v3.4.0）](https://etcd.io/docs/v3.4.0/)
- [ ] [翻译文档（中文）](https://doczhcn.gitbook.io/etcd/)
- [ ] [Github 地址](https://github.com/etcd-io/etcd) <sub> [![Star](https://img.shields.io/github/stars/etcd-io/etcd?style=social&label=Star)](https://github.com/etcd-io/etcd) </sub>
- [ ] [ETCD 原理演示动画（英文）](http://thesecretlivesofdata.com/raft/)
- [ ] Raft 论文：[英文](https://raft.github.io/raft.pdf) · [中文翻译](https://github.com/maemual/raft-zh_cn/blob/master/raft-zh_cn.md)

### Zookeeper

- [ ] 一个分布式的，开放源码的分布式应用程序协调服务
- [ ] [官网（英文）](https://zookeeper.apache.org)
- [ ] [官方文档（英文 v3.5.6）](https://zookeeper.apache.org/doc/r3.5.6/)
- [ ] [翻译文档（中文 from w3cschool）](https://www.w3cschool.cn/zookeeper/zookeeper_overview.html)
- [ ] [Github 地址](https://github.com/apache/zookeeper) <sub> [![Star](https://img.shields.io/github/stars/apache/zookeeper?style=social&label=Star)](https://github.com/apache/zookeeper) </sub>

### Consul

- [ ] 一种服务网格解决方案，提供具有服务发现，配置和分段功能的全功能控制平面
- [ ] [官网（英文）](https://www.consul.io/)
- [ ] [官方文档](https://www.consul.io/docs)
- [ ] [翻译文档（v1.4）](https://kingfree.gitbook.io/consul/)
- [ ] [Github 地址](https://github.com/hashicorp/consul) <sub> [![Star](https://img.shields.io/github/stars/hashicorp/consul?style=social&label=Star)](https://github.com/hashicorp/consul) </sub>

### Nacos

- [ ] 致力于帮助您发现、配置和管理微服务；帮助您更敏捷和容易地构建、交付和管理微服务平台
- [ ] [官网（英文）](https://nacos.io/en-us/index.html)
- [ ] [官网（中文）](https://nacos.io/zh-cn/index.html)
- [ ] [官方文档（英文）](https://nacos.io/en-us/docs/what-is-nacos.html)
- [ ] [官方文档（中文）](https://nacos.io/zh-cn/docs/what-is-nacos.html)
- [ ] [Github 地址](https://github.com/alibaba/nacos) <sub> [![Star](https://img.shields.io/github/stars/alibaba/nacos?style=social&label=Star)](https://github.com/alibaba/nacos) </sub>

### Apollo

- [ ] 携程开源的分布式配置中心，支持多环境、多集群、灰度发布和权限管理，国内使用最广泛的配置中心之一
- [ ] [官网（中文）](https://www.apolloconfig.com/#/zh/README)
- [ ] [官方文档（中文）](https://www.apolloconfig.com/#/zh/documentation/readme)
- [ ] [Github 地址](https://github.com/apolloconfig/apollo) <sub> [![Star](https://img.shields.io/github/stars/apolloconfig/apollo?style=social&label=Star)](https://github.com/apolloconfig/apollo) </sub>

## NoSQL/RDBMS

### Redis

- [ ] 一个开源的，内存中的数据结构存储系统
- [ ] [官网（英文）](https://redis.io)
- [ ] [官网（中文）](http://www.redis.cn)
- [ ] [官方文档（英文）](https://redis.io/documentation)
- [ ] [官方文档（中文）](http://www.redis.cn/documentation.html)
- [ ] [Github 地址](https://github.com/antirez/redis) <sub> [![Star](https://img.shields.io/github/stars/antirez/redis?style=social&label=Star)](https://github.com/antirez/redis) </sub>
- [ ] [在线测试（英文）](https://try.redis.io/)
- [ ] 命令参考（[英文](https://redis.io/commands) · [中文](http://doc.redisfans.com/)）

### MongoDB

- [ ] 一个通用的、基于分布式文件存储的数据库
- [ ] [官网（英文）](https://www.mongodb.com)
- [ ] [官网（中文）](https://www.mongodb.org.cn)
- [ ] [官方教程（英文）](https://docs.mongodb.com/tutorial/)
- [ ] [官方教程（中文）](https://www.mongodb.org.cn/tutorial/)
- [ ] [官方手册（英文）](https://docs.mongodb.com/manual/)
- [ ] [官方手册（中文）](https://www.mongodb.org.cn/manual/)
- [ ] [Github 地址](https://github.com/mongodb/mongo) <sub> [![Star](https://img.shields.io/github/stars/mongodb/mongo?style=social&label=Star)](https://github.com/mongodb/mongo) </sub> 

### Cassandra

- [ ] 一个高度可扩展的分区行存储系统
- [ ] [官网（英文）](https://cassandra.apache.org/)
- [ ] [官方文档（英文）](https://cassandra.apache.org/doc/latest/)
- [ ] [Github 地址](https://github.com/apache/cassandra) <sub> [![Star](https://img.shields.io/github/stars/apache/cassandra?style=social&label=Star)](https://github.com/apache/cassandra) </sub> 

### Memcached

- [ ] 一个高性能的、分布式内存对象缓存系统
- [ ] [官网（英文）](https://memcached.org/)
- [ ] [官方文档（英文）](https://github.com/memcached/memcached/wiki)
- [ ] [Github 地址](https://github.com/memcached/memcached) <sub> [![Star](https://img.shields.io/github/stars/memcached/memcached?style=social&label=Star)](https://github.com/memcached/memcached) </sub> 

### EVCache

- [ ] 基于 memcached 和 spymemcached 的缓存解决方案，主要用于 AWS EC2 基础设施来缓存常用数据
- [ ] [官网：同 Github](https://github.com/Netflix/EVCache)
- [ ] [官方文档（英文）](https://github.com/Netflix/EVCache/wiki)
- [ ] [Github 地址](https://github.com/Netflix/EVCache) <sub> [![Star](https://img.shields.io/github/stars/netflix/evcache?style=social&label=Star)](https://github.com/Netflix/EVCache) </sub> 


### Aerospike

- [ ] ​​第一个 NoSQL 数据库，为始终在线的全球分布式业务交易，在大规模和一致性之间找到了平衡
- [ ] [官网（英文）](https://www.aerospike.com/)
- [ ] [官网（中文）](https://www.aerospike.com/cn/home/)
- [ ] [官方文档（英文）](https://www.aerospike.com/docs/)
- [ ] [Github 地址](https://github.com/aerospike)

### ClickHouse

- [ ] ​​一个开源的、面向列的 OLAP 数据库管理系统，可以实时生成数据分析报告
- [ ] [官网（英文）](https://clickhouse.tech/)
- [ ] [官方文档（英文）](https://clickhouse.tech/docs/en/)
- [ ] [官方文档（中文）](https://clickhouse.tech/docs/zh/)
- [ ] [Github 地址](https://github.com/ClickHouse/ClickHouse) <sub> [![Star](https://img.shields.io/github/stars/ClickHouse/ClickHouse?style=social&label=Star)](https://github.com/ClickHouse/ClickHouse) </sub> 

### OpenTSDB

- [ ] ​​在不丢失粒度的情况下存储和提供大量时间序列数据
- [ ] [官网（英文）](http://opentsdb.net/)
- [ ] [官方文档（英文）](http://opentsdb.net/docs/build/html/index.html)
- [ ] [翻译文档（中文 for v2.3）](https://www.docs4dev.com/docs/zh/opentsdb/2.3/reference/new.html)
- [ ] [Github 地址](https://github.com/OpenTSDB/opentsdb) <sub> [![Star](https://img.shields.io/github/stars/OpenTSDB/opentsdb?style=social&label=Star)](https://github.com/OpenTSDB/opentsdb) </sub> 

### ApacheDruid

- [ ] ​一个高性能的实时分析数据库，可在大规模的负载下对流式传输和批处理数据提供亚秒级查询
- [ ] [官网（英文）](https://druid.apache.org/)
- [ ] [官方文档（英文）](https://druid.apache.org/docs/latest/design/)
- [ ] [翻译文档（中文）](http://www.apache-druid.cn/)
- [ ] [Github 地址](https://github.com/apache/druid) <sub> [![Star](https://img.shields.io/github/stars/apache/druid?style=social&label=Star)](https://github.com/apache/druid) </sub> 

### TiDB

- [ ] 开源分布式 HTAP 数据库，兼容 MySQL 协议，支持水平弹性扩展，同时满足 OLTP 与 OLAP 场景
- [ ] [官网（英文）](https://www.pingcap.com/)
- [ ] [官网（中文）](https://cn.pingcap.com/)
- [ ] [官方文档（英文）](https://docs.pingcap.com/tidb/stable)
- [ ] [官方文档（中文）](https://docs.pingcap.com/zh/tidb/stable)
- [ ] [Github 地址](https://github.com/pingcap/tidb) <sub> [![Star](https://img.shields.io/github/stars/pingcap/tidb?style=social&label=Star)](https://github.com/pingcap/tidb) </sub>

### Neo4j

- [ ] 开源原生图数据库，以节点和关系存储数据，适合社交网络、知识图谱等复杂关系数据分析
- [ ] [官网（英文）](https://neo4j.com/)
- [ ] [官方文档（英文）](https://neo4j.com/docs/)
- [ ] [Github 地址](https://github.com/neo4j/neo4j) <sub> [![Star](https://img.shields.io/github/stars/neo4j/neo4j?style=social&label=Star)](https://github.com/neo4j/neo4j) </sub>

## 监控与显示

### Prometheus

- [ ] 一个开源的监控报警系统和时序列数据库（TSDB）
- [ ] [官网（英文）](https://prometheus.io/)
- [ ] [官方文档（英文）](https://prometheus.io/docs/introduction/overview/)
- [ ] [翻译文档（中文）](https://ryanyang.gitbook.io/prometheus/)
- [ ] [Github 地址](https://github.com/prometheus/prometheus) <sub> [![Star](https://img.shields.io/github/stars/prometheus/prometheus?style=social&label=Star)](https://github.com/prometheus/prometheus) </sub> 

### Grafana

- [ ] 一个开源的度量分析和可视化工具，可以通过将采集的数据查询然后可视化的展示，并及时通知
- [ ] [官网（英文）](https://grafana.com/)
- [ ] [官方文档（英文）](https://grafana.com/docs/)
- [ ] [Github 地址](https://github.com/grafana/grafana) <sub> [![Star](https://img.shields.io/github/stars/grafana/grafana?style=social&label=Star)](https://github.com/grafana/grafana) </sub> 

### Apache SkyWalking

- [ ] 分布式系统应用性能监控工具（APM），支持 Tracing、Metrics、Logging 三位一体可观测，覆盖多语言探针
- [ ] [官网（英文）](https://skywalking.apache.org/)
- [ ] [官方文档（英文）](https://skywalking.apache.org/docs/)
- [ ] [Github 地址](https://github.com/apache/skywalking) <sub> [![Star](https://img.shields.io/github/stars/apache/skywalking?style=social&label=Star)](https://github.com/apache/skywalking) </sub>

### Jaeger

- [ ] Uber 开源的端到端分布式链路追踪系统，已捐赠 CNCF，支持 OpenTelemetry 协议
- [ ] [官网（英文）](https://www.jaegertracing.io/)
- [ ] [官方文档（英文）](https://www.jaegertracing.io/docs/)
- [ ] [Github 地址](https://github.com/jaegertracing/jaeger) <sub> [![Star](https://img.shields.io/github/stars/jaegertracing/jaeger?style=social&label=Star)](https://github.com/jaegertracing/jaeger) </sub>

### OpenTelemetry

- [ ] CNCF 云原生可观测性标准框架，统一 Metrics、Logs、Traces 三类信号的采集、处理与导出规范
- [ ] [官网（英文）](https://opentelemetry.io/)
- [ ] [官网（中文）](https://opentelemetry.io/zh/)
- [ ] [官方文档（英文）](https://opentelemetry.io/docs/)
- [ ] [Github 地址](https://github.com/open-telemetry/opentelemetry-collector) <sub> [![Star](https://img.shields.io/github/stars/open-telemetry/opentelemetry-collector?style=social&label=Star)](https://github.com/open-telemetry/opentelemetry-collector) </sub>

## Web 服务器 / 代理

### Nginx

- [ ] 一个免费的，开源的高性能 HTTP 服务器和反向代理，以及 IMAP/POP3 代理服务器
- [ ] [官网（英文）](https://www.nginx.com/)
- [ ] [中文网站](https://www.nginx.cn/)
- [ ] [官方文档（英文）](https://www.nginx.com/resources/wiki/)
- [ ] [翻译文档（中文）](https://www.nginx.cn/doc/index.html)
- [ ] [Github 地址](https://github.com/nginx/nginx) <sub> [![Star](https://img.shields.io/github/stars/nginx/nginx?style=social&label=Star)](https://github.com/nginx/nginx) </sub> 

### OpenResty

- [ ] 一款基于 NGINX 和 LuaJIT 的 Web 平台
- [ ] [官网（英文）](https://openresty.org/)
- [ ] [官网（中文）](https://openresty.org/cn/)
- [ ] [官方文档（英文）](https://openresty.org/en/getting-started.html)
- [ ] [官方文档（中文）](https://openresty.org/cn/getting-started.html)
- [ ] [Github 地址](https://github.com/openresty) <sub> [![Star](https://img.shields.io/github/stars/openresty/openresty?style=social&label=Star)](https://github.com/openresty/openresty) </sub> 

### Apache_httpd

- [ ] 项目的目标是提供一个安全，高效且可扩展的服务器，该服务器提供与当前HTTP标准同步的 HTTP 服务
- [ ] [官网（英文）](https://httpd.apache.org/)
- [ ] [官方文档（英文）](https://httpd.apache.org/docs/)
- [ ] [官方文档（中文，v2.4 版本，中英文混合）](https://httpd.apache.org/docs/2.4/zh-cn/)
- [ ] [Github 地址](https://github.com/apache/httpd) <sub> [![Star](https://img.shields.io/github/stars/apache/httpd?style=social&label=Star)](https://github.com/apache/httpd) </sub> 

### HAProxy

- [ ] HAProxy 是一款免费的，可为基于 TCP 和 HTTP 的应用程序提供高可用、负载均衡和代理的非常快速且可靠的解决方案。它特别适合于流量非常高的网站，并为世界上许多访问量最大的网站提供支持
- [ ] [官网（英文）](http://www.haproxy.org/)
- [ ] [官方文档（英文）](http://cbonte.github.io/haproxy-dconv/)
- [ ] [Github 地址](https://github.com/haproxy/haproxy) <sub> [![Star](https://img.shields.io/github/stars/haproxy/haproxy?style=social&label=Star)](https://github.com/haproxy/haproxy) </sub> 

### Tengine

- [ ] Tengine 是由淘宝网发起的 Web 服务器项目。它在 Nginx 的基础上，针对大访问量网站的需求，添加了很多高级功能和特性。Tengine 的性能和稳定性已经在大型的网站如淘宝网、天猫商城等得到了很好的检验
- [ ] [官网（中文）](https://tengine.taobao.org/)
- [ ] [官方文档（英文）](https://tengine.taobao.org/documentation.html)
- [ ] [官方文档（中文）](https://tengine.taobao.org/documentation_cn.html)
- [ ] [Github 地址](https://github.com/alibaba/tengine) <sub> [![Star](https://img.shields.io/github/stars/alibaba/tengine?style=social&label=Star)](https://github.com/alibaba/tengine) </sub>

### LVS

- [ ] 具有某些高级功能的 Linux 虚拟服务器发行版。它引入了一种新的数据包转发方法 FULLNAT，以及针对 Synflooding 攻击的防御机制 - SYNPROXY
- [ ] [官网（英文）](http://www.linuxvirtualserver.org/)
- [ ] [官网（中文论坛）](http://zh.linuxvirtualserver.org/)
- [ ] [官方文档（英文）](http://www.linuxvirtualserver.org/Documents.html)
- [ ] [官方文档（中文）](http://linuxvirtualserver.org/zh/index.html)
- [ ] [Github 地址](https://github.com/alibaba/LVS) <sub> [![Star](https://img.shields.io/github/stars/alibaba/LVS?style=social&label=Star)](https://github.com/alibaba/LVS) </sub>

### Keepalived

- [ ] 基于 VRRP 协议，为 Linux 系统和基于 Linux 的基础架构提供负载均衡和高可用性的简单而强大的功能
- [ ] [官网（英文）](https://www.keepalived.org/)
- [ ] [官方文档（英文）](https://www.keepalived.org/manpage.html)
- [ ] [Github 地址](https://github.com/acassen/keepalived) <sub> [![Star](https://img.shields.io/github/stars/acassen/keepalived?style=social&label=Star)](https://github.com/acassen/keepalived) </sub>

## 容器

### Docker

- [ ] 一个开源的应用容器引擎，让开发者可以打包他们的应用以及依赖包到一个可移植的镜像中，然后发布到任何流行的 Linux 或 Windows 机器上
- [ ] [官网（英文）](https://www.docker.com/)
- [ ] [官网（英文）](https://www.docker.com/)
- [ ] [官方文档（英文）](https://docs.docker.com/)
- [ ] [Github 地址](https://github.com/docker) <sub> [![Star](https://img.shields.io/github/stars/docker/docker.github.io?style=social&label=Star)](https://github.com/docker/docker.github.io) </sub> 

### Kubernetes 

- [ ] 一个可移植的、可扩展的开源平台，用于管理容器化的工作负载和服务，可促进声明式配置和自动化
- [ ] [官网（英文）](https://kubernetes.io/)
- [ ] [官网（中文）](https://kubernetes.io/zh/)
- [ ] [官方文档（英文）](https://kubernetes.io/docs/home/)
- [ ] [官方文档（中文）](https://kubernetes.io/zh/docs/home/)
- [ ] [Github 地址](https://github.com/kubernetes/kubernetes) <sub> [![Star](https://img.shields.io/github/stars/kubernetes/kubernetes?style=social&label=Star)](https://github.com/kubernetes/kubernetes) </sub> 

### Kubesphere 

- [ ] 面向云原生应用的容器混合云，愿景是打造一个以 Kubernetes 为内核的云原生分布式操作系统
- [ ] [官网（英文）](https://www.kubesphere.io/)
- [ ] [官网（中文）](https://www.kubesphere.io/zh/)
- [ ] [官方文档（英文）](https://www.kubesphere.io/docs/)
- [ ] [官方文档（中文）](https://www.kubesphere.io/zh/docs/)
- [ ] [Github 地址](https://github.com/kubesphere/kubesphere) <sub> [![Star](https://img.shields.io/github/stars/kubesphere/kubesphere?style=social&label=Star)](https://github.com/kubesphere/kubesphere) </sub> 

### Helm

- [ ] Kubernetes 应用包管理器，通过 Chart 模板标准化应用部署与版本管理
- [ ] [官网（英文）](https://helm.sh/)
- [ ] [官网（中文）](https://helm.sh/zh/)
- [ ] [官方文档（英文）](https://helm.sh/docs/)
- [ ] [官方文档（中文）](https://helm.sh/zh/docs/)
- [ ] [Github 地址](https://github.com/helm/helm) <sub> [![Star](https://img.shields.io/github/stars/helm/helm?style=social&label=Star)](https://github.com/helm/helm) </sub>

### Istio

- [ ] CNCF 开源服务网格，提供流量管理、mTLS 安全通信与可观测能力，无需修改应用代码
- [ ] [官网（英文）](https://istio.io/)
- [ ] [官网（中文）](https://istio.io/zh/)
- [ ] [官方文档（英文）](https://istio.io/latest/docs/)
- [ ] [官方文档（中文）](https://istio.io/zh/docs/)
- [ ] [Github 地址](https://github.com/istio/istio) <sub> [![Star](https://img.shields.io/github/stars/istio/istio?style=social&label=Star)](https://github.com/istio/istio) </sub>

### Harbor

- [ ] CNCF 毕业的开源企业级容器镜像仓库，支持镜像安全扫描、RBAC 访问控制与多副本同步
- [ ] [官网（英文）](https://goharbor.io/)
- [ ] [官方文档（英文）](https://goharbor.io/docs/)
- [ ] [Github 地址](https://github.com/goharbor/harbor) <sub> [![Star](https://img.shields.io/github/stars/goharbor/harbor?style=social&label=Star)](https://github.com/goharbor/harbor) </sub>

### Argo CD

- [ ] 基于 GitOps 的 Kubernetes 声明式持续交付工具，以 Git 仓库为唯一真相源，自动同步集群状态
- [ ] [官网（英文）](https://argo-cd.readthedocs.io/)
- [ ] [官方文档（英文）](https://argo-cd.readthedocs.io/en/stable/)
- [ ] [Github 地址](https://github.com/argoproj/argo-cd) <sub> [![Star](https://img.shields.io/github/stars/argoproj/argo-cd?style=social&label=Star)](https://github.com/argoproj/argo-cd) </sub>

## CI/CD/质量管理

### Jenkins 

- [ ] 一个提供友好操作界面的持续集成工具
- [ ] [官网（英文）](https://www.jenkins.io/)
- [ ] [官网（中文）](https://www.jenkins.io/zh/)
- [ ] [官方文档（英文）](https://www.jenkins.io/doc/)
- [ ] [官方文档（中文）](https://www.jenkins.io/zh/doc/)
- [ ] [Github 地址](https://github.com/jenkinsci/jenkins) <sub> [![Star](https://img.shields.io/github/stars/jenkinsci/jenkins?style=social&label=Star)](https://github.com/jenkinsci/jenkins) </sub> 

### SonarQube 

- [ ] 一个用于代码质量管理的开放平台
- [ ] [官网（英文）](https://www.sonarqube.org/)
- [ ] [官方文档（英文）](https://docs.sonarqube.org/latest/)
- [ ] [Github 地址](https://github.com/SonarSource/sonarqube) <sub> [![Star](https://img.shields.io/github/stars/SonarSource/sonarqube?style=social&label=Star)](https://github.com/SonarSource/sonarqube) </sub> 

### Spinnaker 

- [ ] 一个开源的持续交付平台，用于快速、可靠地发布软件更改
- [ ] [官网（英文）](https://spinnaker.io/)
- [ ] [官方文档（英文）](https://spinnaker.io/guides/)
- [ ] [Github 地址](https://github.com/spinnaker/spinnaker) <sub> [![Star](https://img.shields.io/github/stars/spinnaker/spinnaker?style=social&label=Star)](https://github.com/spinnaker/spinnaker) </sub> 

### SerenityBDD 

- [ ] 一个测试自动化库，旨在简化编写自动验收测试的过程，并使其更加有趣（UI 测试）
- [ ] [官网（英文）](http://serenity-bdd.info/)
- [ ] [官方文档（英文）](http://serenity-bdd.info/#/documentation)
- [ ] [Github 地址](https://github.com/serenity-bdd) <sub> [![Star](https://img.shields.io/github/stars/serenity-bdd/serenity-core?style=social&label=Star)](https://github.com/serenity-bdd/serenity-core) </sub> 

## 对象存储

### MinIO

- [ ] 高性能 S3 兼容对象存储，适用于 AI/ML 数据湖场景，支持单节点到多节点分布式部署
- [ ] [官网（英文）](https://min.io/)
- [ ] [官网（中文）](https://www.minio.org.cn/)
- [ ] [官方文档（英文）](https://min.io/docs/minio/linux/index.html)
- [ ] [Github 地址](https://github.com/minio/minio) <sub> [![Star](https://img.shields.io/github/stars/minio/minio?style=social&label=Star)](https://github.com/minio/minio) </sub>

## API 网关

### Apache APISIX

- [ ] 云原生高性能 API 网关，支持动态路由、插件热加载与 gRPC/WebSocket，已捐赠 Apache
- [ ] [官网（英文）](https://apisix.apache.org/)
- [ ] [官网（中文）](https://apisix.apache.org/zh/)
- [ ] [官方文档（英文）](https://apisix.apache.org/docs/apisix/getting-started/)
- [ ] [官方文档（中文）](https://apisix.apache.org/zh/docs/apisix/getting-started/)
- [ ] [Github 地址](https://github.com/apache/apisix) <sub> [![Star](https://img.shields.io/github/stars/apache/apisix?style=social&label=Star)](https://github.com/apache/apisix) </sub>

### Kong

- [ ] 云原生 API 网关与服务连接平台，插件生态丰富，支持 Kubernetes Ingress 和声明式配置
- [ ] [官网（英文）](https://konghq.com/)
- [ ] [官方文档（英文）](https://docs.konghq.com/)
- [ ] [Github 地址](https://github.com/Kong/kong) <sub> [![Star](https://img.shields.io/github/stars/Kong/kong?style=social&label=Star)](https://github.com/Kong/kong) </sub>

### Traefik

- [ ] 云原生应用代理，支持自动服务发现与动态配置，与 Docker、Kubernetes 深度集成，零重启热更新
- [ ] [官网（英文）](https://traefik.io/)
- [ ] [官方文档（英文）](https://doc.traefik.io/traefik/)
- [ ] [Github 地址](https://github.com/traefik/traefik) <sub> [![Star](https://img.shields.io/github/stars/traefik/traefik?style=social&label=Star)](https://github.com/traefik/traefik) </sub>

## 任务调度

### XXL-JOB

- [ ] 轻量级分布式任务调度平台，提供可视化管理界面，开箱即用，国内使用广泛
- [ ] [官网（中文）](https://www.xuxueli.com/xxl-job/)
- [ ] [官方文档（中文）](https://www.xuxueli.com/xxl-job/)
- [ ] [Github 地址](https://github.com/xuxueli/xxl-job) <sub> [![Star](https://img.shields.io/github/stars/xuxueli/xxl-job?style=social&label=Star)](https://github.com/xuxueli/xxl-job) </sub>

### Apache DolphinScheduler

- [ ] 云原生分布式可视化工作流调度平台，支持 DAG 依赖编排，覆盖数据管道全生命周期管理
- [ ] [官网（英文）](https://dolphinscheduler.apache.org/)
- [ ] [官网（中文）](https://dolphinscheduler.apache.org/zh-cn/)
- [ ] [官方文档（英文）](https://dolphinscheduler.apache.org/en-us/docs/latest/user_doc/about/introduction.html)
- [ ] [官方文档（中文）](https://dolphinscheduler.apache.org/zh-cn/docs/latest/user_doc/about/introduction.html)
- [ ] [Github 地址](https://github.com/apache/dolphinscheduler) <sub> [![Star](https://img.shields.io/github/stars/apache/dolphinscheduler?style=social&label=Star)](https://github.com/apache/dolphinscheduler) </sub>

## 安全与认证

### Keycloak

- [ ] 开源身份认证与访问管理系统，支持 SSO、OAuth2、OIDC 和 SAML，提供用户联邦与社交登录
- [ ] [官网（英文）](https://www.keycloak.org/)
- [ ] [官方文档（英文）](https://www.keycloak.org/documentation)
- [ ] [Github 地址](https://github.com/keycloak/keycloak) <sub> [![Star](https://img.shields.io/github/stars/keycloak/keycloak?style=social&label=Star)](https://github.com/keycloak/keycloak) </sub>

### HashiCorp Vault

- [ ] 基于身份的密钥与敏感数据安全管理工具，支持动态凭证生成、数据加密即服务与密钥轮换
- [ ] [官网（英文）](https://www.vaultproject.io/)
- [ ] [官方文档（英文）](https://developer.hashicorp.com/vault/docs)
- [ ] [Github 地址](https://github.com/hashicorp/vault) <sub> [![Star](https://img.shields.io/github/stars/hashicorp/vault?style=social&label=Star)](https://github.com/hashicorp/vault) </sub>

## 基础原理可视化

- [B+Trees](https://www.cs.usfca.edu/~galles/visualization/BPlusTree.html)
- [B-Trees](https://www.cs.usfca.edu/~galles/visualization/BTree.html)
- [Raft（主节点的选举过程动画）](https://raft.github.io/)
