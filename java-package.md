# Jar package

收集优秀的第三方 jar 包。国内 Maven 仓库推荐使用 aliyun 仓库，以提高下载 jar 包速度。配置方法参见：[Maven：配置 aliyun 仓库](https://github.com/kenttanl/iDocuments/issues/1)。

## Utils

### guava

- Google 的开源工具类
- [Github 地址](https://github.com/google/guava)
- [官方教程（英文）](https://github.com/google/guava/wiki)
- [官方教程（中文）](https://wizardforcel.gitbooks.io/guava-tutorial/content/1.html)
- [Maven or Gradle](https://github.com/google/guava/wiki/UseGuavaInYourBuild)
- groupId.artifactId: com.google.guava

### commons-lang3

- 标准 Java 库未能提供足够的方法来操作其核心类。Apache Commons Lang 提供了这些额外的方法。
- [官方文档（英文）](http://commons.apache.org/proper/commons-lang/index.html)
- groupId.artifactId: org.apache.commons.commons-lang3

### jasypt

- 便捷的加密库，可对配置文件中的数据库密码加密
- [官网（英文）](http://www.jasypt.org)
- [Github 地址：jasypt-spring-boot](https://github.com/ulisesbocchio/jasypt-spring-boot)
- [Maven for not spring-boot](http://www.jasypt.org/maven.html)
- groupId.artifactId: com.zaxxer.HikariCP

### liquibase

- 一个用于跟踪、管理和应用数据库变化的开源的数据库重构工具
- [官网（英文）](http://www.liquibase.org)

### HikariCP

- 一个可靠的、高性能的 JDBC 连接池
- [Github 地址](https://github.com/brettwooldridge/HikariCP)
- groupId.artifactId: org.jasypt.jasypt

## Client

### Kafka

- kafka-clients: 
  - 原生的 Kafka client
  - [官方文档（中文）](http://kafka.apachecn.org/documentation.html#api)
  - org.apache.kafka.kafka-clients
- spring-kafka: 
  - Spring 封装后的 client
  - [官方文档（英文）](https://spring.io/projects/spring-kafka)
  - org.springframework.kafka


