# 如何确认MRS Manger的主备管理节点<a name="ZH-CN_TOPIC_0173178750"></a>

介绍如何在Master1节点中确认MRS Manager的主备管理节点。

## 背景信息<a name="section3630089719169"></a>

用户可以在Master节点登录到集群中的其他节点，同时登录Master节点后，可以确认MRS Manager的主备管理节点，并在对应的管理节点中执行命令。

在主备模式下，由于Master1和Master2之间会切换，Master1节点不一定是MRS Manager的主管理节点。

## 操作步骤<a name="section27848344191744"></a>

1.  确认MRS集群的Master节点。
    1.  登录MapReduce服务管理控制台，选择“集群列表 \> 现有集群“，选中一个运行中的集群并单击集群名，进入集群信息页面。查看指定的集群信息。
    2.  在“节点信息“中查看节点名称，名称中包含“master1“的节点为Master1节点，名称中包含“master2“的节点为Master2节点。

2.  确认MRS Manager的主备管理节点。
    1.  远程登录Master1节点，请参见[登录集群节点](登录集群节点.md)。

        针对MRS1.6.2版本（不包含）前的集群，Master节点支持Cloud-Init特性，Cloud-init预配置的用户名“linux“，密码默认为“cloud.1234“，如果用户修改了默认密码请使用新密码。首次登录建议修改。

        针对MRS1.6.2版本（包含）及以后的集群，Master节点支持Cloud-Init特性，Cloud-init预配置的用户名“root“，密码为创建集群时设置的密码。

    2.  执行以下命令切换用户。

        **sudo su - root**

        **su - omm**

    3.  执行以下命令确认主备管理节点：

        **sh $\{BIGDATA\_HOME\}/om-0.0.1/sbin/status-oms.sh**

        回显信息中“HAActive”参数值为“active”的节点为主管理节点（如下例中“mgtomsdat-sh-3-01-1”为主管理节点），参数值为“standby”的节点为备管理节点（如下例中“mgtomsdat-sh-3-01-2”为备管理节点）。

        ```
        Ha mode
        double
        NodeName              HostName                      HAVersion          StartTime                HAActive             HAAllResOK           HARunPhase 
        192-168-0-30          mgtomsdat-sh-3-01-1           V100R001C01        2014-11-18 23:43:02      active               normal               Actived    
        192-168-0-24          mgtomsdat-sh-3-01-2           V100R001C01        2014-11-21 07:14:02      standby              normal               Deactived
        ```

        >![](public_sys-resources/icon-note.gif) **说明：**   
        >如果当前登录的Master1节点是备管理节点，且需要登录到主管理节点时，请执行以下命令：  
        >**ssh** _Master2节点IP地址_  



