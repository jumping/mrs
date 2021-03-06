# 14\_MRS故障排除

-   [使用HBase]
    -   [连接到HBase响应慢](连接到HBase响应慢.md)
    -   [HBase用户认证失败](HBase用户认证失败.md)
    -   [端口被占用导致RegionServer启动失败](端口被占用导致RegionServer启动失败.md)
    -   [节点剩余内存不足导致HBase启动失败](节点剩余内存不足导致HBase启动失败.md)
    -   [HDFS性能差导致HBase服务不可用告警](HDFS性能差导致HBase服务不可用告警.md)
    -   [参数不合理导致HBase启动失败](参数不合理导致HBase启动失败.md)
    -   [残留进程导致Regionsever启动失败](残留进程导致Regionsever启动失败.md)
    -   [HDFS上设置配额导致HBase启动失败](HDFS上设置配额导致HBase启动失败.md)
    -   [HBase的initial超时保留导致启动失败](HBase的initial超时保留导致启动失败.md)
    -   [HBase version文件损坏导致启动失败](HBase-version文件损坏导致启动失败.md)
    -   [无业务情况下，RegionServer占用CPU高](无业务情况下-RegionServer占用CPU高.md)
    -   [HBase启动失败，RegionServer日志中提示FileNotFoundException异常](HBase启动失败-RegionServer日志中提示FileNotFoundException异常.md)
    -   [HBase启动后原生页面显示RegionServer个数多于实际个数](HBase启动后原生页面显示RegionServer个数多于实际个数.md)
    -   [RegionServer实例异常，处于Concerning状态](RegionServer实例异常-处于Concerning状态.md)
    -   [新安装的集群HBase启动失败](新安装的集群HBase启动失败.md)
    -   [acl表目录丢失导致HBase启动失败](acl表目录丢失导致HBase启动失败.md)
    -   [集群上下电之后HBase启动失败](集群上下电之后HBase启动失败.md)
    -   [HBase异常](HBase异常.md)

-   [使用Hive]
    -   [Hive各个日志里都存放了什么信息？](Hive各个日志里都存放了什么信息.md)
    -   [Hive启动失败问题的原因有哪些？](Hive启动失败问题的原因有哪些.md)
    -   [安全集群执行set命令的时候报Cannot modify xxx at runtime.](安全集群执行set命令的时候报Cannot-modify-xxx-at-runtime.md)
    -   [怎样在Hive提交任务的时候指定队列？](怎样在Hive提交任务的时候指定队列.md)
    -   [客户端怎么设置Map/Reduce内存？](客户端怎么设置Map-Reduce内存.md)
    -   [如何在导入表时指定输出的文件压缩格式](如何在导入表时指定输出的文件压缩格式.md)
    -   [desc描述表过长时，无法显示完整](desc描述表过长时-无法显示完整.md)
    -   [增加分区列后再insert数据显示为NULL](增加分区列后再insert数据显示为NULL.md)
    -   [创建新用户，执行查询时报无权限](创建新用户-执行查询时报无权限.md)
    -   [执行SQL提交任务到指定队列报错](执行SQL提交任务到指定队列报错.md)
    -   [执行load data inpath命令报错](执行load-data-inpath命令报错.md)
    -   [执行load data local inpath命令报错](执行load-data-local-inpath命令报错.md)
    -   [执行create external table报错](执行create-external-table报错.md)
    -   [在beeline客户端执行dfs -put命令报错](在beeline客户端执行dfs--put命令报错.md)
    -   [执行set role admin报无权限](执行set-role-admin报无权限.md)
    -   [通过beeline创建UDF时候报错](通过beeline创建UDF时候报错.md)
    -   [Hive状态为Bad问题总结](Hive状态为Bad问题总结.md)
    -   [Hive服务状态为Partially Healthy总结](Hive服务状态为Partially-Healthy总结.md)
    -   [Hive服务健康状态和Hive实例健康状态的区别](Hive服务健康状态和Hive实例健康状态的区别.md)
    -   [Hive中的告警有哪些以及触发的场景](Hive中的告警有哪些以及触发的场景.md)
    -   [Shell客户端连接提示"authentication failed"](Shell客户端连接提示-authentication-failed.md)
    -   [客户端提示访问ZooKeeper失败](客户端提示访问ZooKeeper失败.md)
    -   [使用udf函数提示"Invalid function"](使用udf函数提示-Invalid-function.md)
    -   [Hive服务状态为Unknown总结](Hive服务状态为Unknown总结.md)
    -   [Hiveserver或者Metastore实例的健康状态为unknown](Hiveserver或者Metastore实例的健康状态为unknown.md)
    -   [Hiveserver或者Metastore实例的健康状态为Concerning](Hiveserver或者Metastore实例的健康状态为Concerning.md)
    -   [TEXTFILE类型文件使用ARC4压缩时select结果乱码](TEXTFILE类型文件使用ARC4压缩时select结果乱码.md)
    -   [hive任务运行过程中失败，重试成功](hive任务运行过程中失败-重试成功.md)
    -   [执行select语句报错](执行select语句报错.md)
    -   [drop partition操作，有大量分区时操作失败](drop-partition操作-有大量分区时操作失败.md)
    -   [localtask启动失败](localtask启动失败.md)
    -   [WebHCat启动失败](WebHCat启动失败.md)
    -   [切域后Hive二次开发样例代码报错](切域后Hive二次开发样例代码报错.md)
    -   [DBService超过最大连接数，导致metastore异常](DBService超过最大连接数-导致metastore异常.md)
    -   [Beeline报Failed to execute session hooks: over max connections错误](Beeline报Failed-to-execute-session-hooks-over-max-connections错误.md)
    -   [Beeline报OutOfMemoryError错误](Beeline报OutOfMemoryError错误.md)
    -   [输入文件数超出设置限制导致任务执行失败](输入文件数超出设置限制导致任务执行失败.md)
    -   [任务执行中报栈内存溢出导致任务执行失败](任务执行中报栈内存溢出导致任务执行失败.md)
    -   [对同一张表或分区并发写数据导致任务失败](对同一张表或分区并发写数据导致任务失败.md)
    -   [Hive任务失败，报没有HDFS目录的权限](Hive任务失败-报没有HDFS目录的权限.md)
    -   [Load数据到Hive表失败](Load数据到Hive表失败.md)
    -   [参考Hive JDBC代码用例开发的业务应用运行失败](参考Hive-JDBC代码用例开发的业务应用运行失败.md)
    -   [HiveServer和HiveHCat进程故障](HiveServer和HiveHCat进程故障.md)

-   [使用Spark]
    -   [Spark应用下修改split值时报错](Spark应用下修改split值时报错.md)
    -   [使用Spark时报错](使用Spark时报错.md)
    -   [磁盘容量不足，导致Spark、Hive和Yarn服务不可用](磁盘容量不足-导致Spark-Hive和Yarn服务不可用.md)
    -   [引入jar包不正确，导致Spark任务无法运行](引入jar包不正确-导致Spark任务无法运行.md)
    -   [Spark任务由于内存不够，作业卡住](Spark任务由于内存不够-作业卡住.md)
    -   [运行Spark报错](运行Spark报错.md)
    -   [Driver端提示executor memory超限](Driver端提示executor-memory超限.md)
    -   [Yarn-cluster模式下，Can't get the Kerberos realm异常](Yarn-cluster模式下-Can-t-get-the-Kerberos-realm异常.md)
    -   [JDK版本不匹配启动spark-sql，spark-shell失败](JDK版本不匹配启动spark-sql-spark-shell失败.md)
    -   [Yarn-client模式提交ApplicationMaster尝试启动两次失败](Yarn-client模式提交ApplicationMaster尝试启动两次失败.md)
    -   [提交Spark任务时，连接ResourceManager异常](提交Spark任务时-连接ResourceManager异常.md)
    -   [DaYu调度spark作业失败](DaYu调度spark作业失败.md)

-   [使用Kafka]
    -   [运行Kafka获取topic报错](运行Kafka获取topic报错.md)
    -   [安全集群中如何使用Python3.x对接Kafka？](安全集群中如何使用Python3-x对接Kafka.md)
    -   [Flume可以正常连接Kafka，但是发送消息失败。](Flume可以正常连接Kafka-但是发送消息失败.md)
    -   [Producer发送数据失败，抛出NullPointerException](Producer发送数据失败-抛出NullPointerException.md)
    -   [Producer发送数据失败，抛出TOPIC\_AUTHORIZATION\_FAILED](Producer发送数据失败-抛出TOPIC_AUTHORIZATION_FAILED.md)
    -   [Producer偶现发送数据失败，日志提示Too many open files in system](Producer偶现发送数据失败-日志提示Too-many-open-files-in-system.md)
    -   [Consumer初始化成功，但是无法从Kafka中获取指定Topic消息](Consumer初始化成功-但是无法从Kafka中获取指定Topic消息.md)
    -   [Consumer消费数据失败，Consumer一直处于等待状态 ](Consumer消费数据失败-Consumer一直处于等待状态.md)
    -   [SparkStreaming消费Kafka消息失败，提示Error getting partition metadata ](SparkStreaming消费Kafka消息失败-提示Error-getting-partition-metadata.md)
    -   [新建集群Consumer消费数据失败，提示GROUP\_COORDINATOR\_NOT\_AVAILABLE](新建集群Consumer消费数据失败-提示GROUP_COORDINATOR_NOT_AVAILABLE.md)
    -   [SparkStreaming消费Kafka消息失败，提示Couldn't find leader offsets](SparkStreaming消费Kafka消息失败-提示Couldn-t-find-leader-offsets.md)
    -   [Consumer消费数据失败，提示SchemaException: Error reading field 'brokers'](Consumer消费数据失败-提示SchemaException-Error-reading-field-brokers.md)
    -   [Consumer消费数据是否丢失排查](Consumer消费数据是否丢失排查.md)
    -   [账号锁定导致启动组件失败](账号锁定导致启动组件失败.md)
    -   [Kafka Broker上报进程异常，日志提示IllegalArgumentException](Kafka-Broker上报进程异常-日志提示IllegalArgumentException.md)
    -   [执行Kafka Topic删除操作，发现无法删除](执行Kafka-Topic删除操作-发现无法删除.md)
    -   [执行Kafka Topic删除操作，提示AdminOperationException](执行Kafka-Topic删除操作-提示AdminOperationException.md)
    -   [执行Kafka Topic创建操作，发现无法创建提示NoAuthException](执行Kafka-Topic创建操作-发现无法创建提示NoAuthException.md)
    -   [执行Kafka Topic设置ACL操作失败，提示NoAuthException](执行Kafka-Topic设置ACL操作失败-提示NoAuthException.md)
    -   [执行Kafka Topic创建操作，发现无法创建提示NoNode for /brokers/ids](执行Kafka-Topic创建操作-发现无法创建提示NoNode-for-brokers-ids.md)
    -   [执行Kakfa Topic创建操作，发现无法创建提示replication factor larger than available brokers](执行Kakfa-Topic创建操作-发现无法创建提示replication-factor-larger-than-available-brokers.md)
    -   [Consumer消费数据存在重复消费现象](Consumer消费数据存在重复消费现象.md)
    -   [执行Kafka Topic创建操作，发现节点上Partition数量分布不均衡](执行Kafka-Topic创建操作-发现节点上Partition数量分布不均衡.md)
    -   [执行Kafka Topic创建操作，发现Partition的Leader显示为none](执行Kafka-Topic创建操作-发现Partition的Leader显示为none.md)
    -   [Kafka安全使用说明](Kafka安全使用说明.md)
    -   [如何获取Kafka Consumer Offset信息](如何获取Kafka-Consumer-Offset信息.md)
    -   [如何针对Topic进行配置增加和删除](如何针对Topic进行配置增加和删除.md)
    -   [如何读取“\_\_consumer\_offsets”内部topic的内容](如何读取-__consumer_offsets-内部topic的内容.md)
    -   [如何配置客户端shell命令的日志](如何配置客户端shell命令的日志.md)
    -   [如何获取Topic的分布信息](如何获取Topic的分布信息.md)
    -   [Kafka高可靠使用说明](Kafka高可靠使用说明.md)
    -   [使用Kafka Shell命令无法操作Kafka集群](使用Kafka-Shell命令无法操作Kafka集群.md)
    -   [Kafka生产者写入单条记录过长问题](Kafka生产者写入单条记录过长问题.md)
    -   [Kakfa消费者读取单条记录过长问题](Kakfa消费者读取单条记录过长问题.md)

-   [使用Storm]
    -   [Storm组件的Storm UI页面中events超链接地址无效](Storm组件的Storm-UI页面中events超链接地址无效.md)
    -   [提交拓扑失败](提交拓扑失败.md)
    -   [提交拓扑失败，提示Failed to check principle for keytab](提交拓扑失败-提示Failed-to-check-principle-for-keytab.md)
    -   [提交拓扑后Worker日志为空](提交拓扑后Worker日志为空.md)
    -   [提交拓扑后Worker运行异常，日志提示Failed to bind to：host:ip](提交拓扑后Worker运行异常-日志提示Failed-to-bind-to-host-ip.md)
    -   [使用jstack命令查看进程堆栈提示well-known file is not secure](使用jstack命令查看进程堆栈提示well-known-file-is-not-secure.md)
    -   [使用Storm-JDBC插件开发Oracle写入Bolt，发现数据无法写入](使用Storm-JDBC插件开发Oracle写入Bolt-发现数据无法写入.md)
    -   [业务拓扑配置GC参数不生效](业务拓扑配置GC参数不生效.md)
    -   [UI查看信息显示Internal Server Error](UI查看信息显示Internal-Server-Error.md)

-   [使用Flume]
    -   [Flume向Spark Streaming提交作业，提交到集群后报类找不到](Flume向Spark-Streaming提交作业-提交到集群后报类找不到.md)
    -   [Flume客户端安装失败](Flume客户端安装失败.md)
    -   [Flume客户端无法连接服务端](Flume客户端无法连接服务端.md)
    -   [Flume数据写入组件失败](Flume数据写入组件失败.md)
    -   [Flume 服务端进程故障](Flume-服务端进程故障.md)
    -   [Flume数据采集慢](Flume数据采集慢.md)
    -   [Flume启动失败](Flume启动失败.md)

-   [使用Hue]
    -   [Hue上有job在运行](Hue上有job在运行.md)
    -   [使用IE浏览器在Hue中执行HQL失败](使用IE浏览器在Hue中执行HQL失败.md)
    -   [Hue（主）无法打开web网页](Hue（主）无法打开web网页.md)
    -   [Hue WebUI访问失败](Hue-WebUI访问失败.md)
    -   [Hue界面无法加载HBase表](Hue界面无法加载HBase表.md)

-   [使用HDFS]
    -   [修改集群HDFS服务的NameNode RPC端口后，NameNode都变为备状态](修改集群HDFS服务的NameNode-RPC端口后-NameNode都变为备状态.md)
    -   [通过公网IP连接主机，使用HDFS客户端报错](通过公网IP连接主机-使用HDFS客户端报错.md)
    -   [使用Python远程连接HDFS的端口失败](使用Python远程连接HDFS的端口失败.md)
    -   [HDFS容量使用达到100%，导致上层服务HBase、Spark等上报服务不可用](HDFS容量使用达到100-导致上层服务HBase-Spark等上报服务不可用.md)
    -   [启动HDFS和Yarn报错](启动HDFS和Yarn报错.md)
    -   [HDFS权限设置问题](HDFS权限设置问题.md)
    -   [HDFS的DataNode一直显示退服中](HDFS的DataNode一直显示退服中.md)
    -   [内存不足导致HDFS启动失败](内存不足导致HDFS启动失败.md)
    -   [ntpdate修改时间导致HDFS出现大量丢块](ntpdate修改时间导致HDFS出现大量丢块.md)
    -   [DataNode概率性出现CPU占用接近100%，导致节点丢失（ssh连得很慢或者不上）](DataNode概率性出现CPU占用接近100-导致节点丢失（ssh连得很慢或者不上）.md)
    -   [单NameNode长期故障，如何使用客户端手动checkpoint](单NameNode长期故障-如何使用客户端手动checkpoint.md)
    -   [文件读写常见故障](文件读写常见故障.md)
    -   [文件最大打开句柄数设置太小导致读写文件异常](文件最大打开句柄数设置太小导致读写文件异常.md)
    -   [客户端写文件close失败](客户端写文件close失败.md)
    -   [文件错误导致上传文件到HDFS失败](文件错误导致上传文件到HDFS失败.md)
    -   [界面配置dfs.blocksize后put数据，block大小还是原来的大小](界面配置dfs-blocksize后put数据-block大小还是原来的大小.md)
    -   [读取文件失败，FileNotFoundException](读取文件失败-FileNotFoundException.md)
    -   [HDFS写文件失败，item limit of / is exceeded](HDFS写文件失败-item-limit-of-is-exceeded.md)
    -   [调整shell客户端日志级别](调整shell客户端日志级别.md)
    -   [读文件失败No common protection layer](读文件失败No-common-protection-layer.md)
    -   [HDFS目录配额（quota）不足导致写文件失败](HDFS目录配额（quota）不足导致写文件失败.md)
    -   [执行balance失败，Source and target differ in block-size](执行balance失败-Source-and-target-differ-in-block-size.md)
    -   [查询或者删除文件失败，父目录可以看见此文件（不可见字符）](查询或者删除文件失败-父目录可以看见此文件（不可见字符）.md)
    -   [非HDFS数据残留导致数据分布不均衡](非HDFS数据残留导致数据分布不均衡.md)
    -   [客户端安装在数据节点导致数据分布不均衡](客户端安装在数据节点导致数据分布不均衡.md)
    -   [节点内DataNode磁盘使用率不均衡处理指导](节点内DataNode磁盘使用率不均衡处理指导.md)
    -   [执行balance常见问题定位方法](执行balance常见问题定位方法.md)
    -   [HDFS显示磁盘空间不足，其实还有10%磁盘空间](HDFS显示磁盘空间不足-其实还有10-磁盘空间.md)
    -   [普通集群在Core节点安装hdfs客户端，使用时报错](普通集群在Core节点安装hdfs客户端-使用时报错.md)

-   [使用Yarn]
    -   [启动Yarn后发现一堆job](启动Yarn后发现一堆job.md)
    -   [通过客户端hadoop jar命令提交任务，客户端返回GC overhead](通过客户端hadoop-jar命令提交任务-客户端返回GC-overhead.md)

-   [使用DBservice]
    -   [DBServer实例状态异常](DBServer实例状态异常.md)
    -   [DBServer实例一直处于Concerning状态](DBServer实例一直处于Concerning状态.md)
    -   [默认端口20050或20051被占用](默认端口20050或20051被占用.md)
    -   [/tmp目录权限不对导致DBserver实例状态一直处于Concerning ](tmp目录权限不对导致DBserver实例状态一直处于Concerning.md)
    -   [DBService备份失败](DBService备份失败.md)
    -   [DBService状态正常，组件无法连接DBService](DBService状态正常-组件无法连接DBService.md)
    -   [DBServer启动失败](DBServer启动失败.md)
    -   [浮动IP不通导致DBService备份失败](浮动IP不通导致DBService备份失败.md)
    -   [DBService配置文件丢失导致启动失败](DBService配置文件丢失导致启动失败.md)

-   [使用Flink]
    -   [安装客户端执行命令错误，提示IllegalConfigurationException: Error while parsing YAML configuration file :"security.kerberos.login.keytab"](安装客户端执行命令错误-提示IllegalConfigurationException-Error-while-parsing-YAML-configuration-file-security-ker.md)
    -   [安装客户端修改配置后执行命令错误，提示IllegalConfigurationException: Error while parsing YAML configuration file](安装客户端修改配置后执行命令错误-提示IllegalConfigurationException-Error-while-parsing-YAML-configuration-file.md)
    -   [创建Flink集群时执行yarn-session.sh命令失败](创建Flink集群时执行yarn-session-sh命令失败.md)
    -   [使用不同用户，执行yarn-session创建集群失败](使用不同用户-执行yarn-session创建集群失败.md)
    -   [Flink业务程序无法读取NFS盘上的文件](Flink业务程序无法读取NFS盘上的文件.md)

-   [使用Impala]
    -   [用户连接impala-shell失败](用户连接impala-shell失败.md)

-   [使用Presto]
    -   [配置sql-standard-with-group创建schema失败报Access Denied](配置sql-standard-with-group创建schema失败报Access-Denied.md)

-   [使用Alluixo]
    -   [Alluixo在HA模式下出现Does not contain a valid host:port authority报错](Alluixo在HA模式下出现Does-not-contain-a-valid-host-port-authority报错.md)

-   [使用ZooKeeper]
    -   [MRS集群如何访问zookeeper](MRS集群如何访问zookeeper.md)

-   [管理数据]
    -   [缩容Task节点失败](缩容Task节点失败.md)
    -   [如何处理集群内部OBS证书过期](如何处理集群内部OBS证书过期.md)
    -   [MRS集群添加新磁盘](MRS集群添加新磁盘.md)
    -   [MRS集群更换磁盘](MRS集群更换磁盘.md)
    -   [MRS备份失败](MRS备份失败.md)
    -   [Core节点出现df显示的容量和du显示的容量不一致](Core节点出现df显示的容量和du显示的容量不一致.md)

-   [连接网络]
    -   [如何解除关联子网](如何解除关联子网.md)
    -   [外网能否连接MRS](外网能否连接MRS.md)
    -   [使用AK/SK获取MRS集群主机列表接口时提示用户无权限“User do not have right to access cluster”](使用AK-SK获取MRS集群主机列表接口时提示用户无权限-User-do-not-have-right-to-access-cluster.md)
    -   [Mac如何访问MRS Manager](Mac如何访问MRS-Manager.md)

-   [集群管理]
    -   [忘记admin密码，如何重置或修改？](忘记admin密码-如何重置或修改.md)

-   [集群异常]
    -   [升级Python后，无法登录MRS Manager页面](升级Python后-无法登录MRS-Manager页面.md)
    -   [修改hostname，导致MRS状态异常](修改hostname-导致MRS状态异常.md)
    -   [调用API接口创建集群失败](调用API接口创建集群失败.md)
    -   [如何定位进程被kill](如何定位进程被kill.md)
    -   [配置跨集群互信失败](配置跨集群互信失败.md)
    -   [MRS 集群使用pip3安装python包提示网络不可达](MRS-集群使用pip3安装python包提示网络不可达.md)


