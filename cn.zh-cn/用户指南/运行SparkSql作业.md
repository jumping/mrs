# 运行SparkSql作业<a name="ZH-CN_TOPIC_0173264855"></a>

用户可将自己开发的程序提交到MRS中，执行程序并获取结果。本章节教您在MRS集群页面如何提交一个新的SparkSql作业。SparkSql作业用于查询和分析数据，包括SQL语句和Script脚本两种形式，如果SQL语句涉及敏感信息，请使用Spark Script提交。

## 前提条件<a name="section2335951116026"></a>

用户已经将运行作业所需的程序包和数据文件上传至OBS系统或HDFS中。

## 通过界面提交作业<a name="section75299125395"></a>

1.  登录MRS管理控制台。
2.  选择“集群列表 \> 现有集群”，选中一个运行中的集群并单击集群名称，进入集群信息页面。
3.  若集群开启Kerberos认证时执行该步骤，若集群未开启Kerberos认证，请无需执行该步骤。

    在“概览“页签的基本信息区域，单击“IAM用户同步“右侧的![](figures/zh-cn_image_0182828410.png)进行IAM用户同步，具体介绍请参考[IAM用户同步MRS](IAM用户同步MRS.md)。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   MRS 1.8.7之前版本或者MRS 2.0.1版本开启Kerberos认证集群不支持“作业管理”功能，请通过后台功能提交作业。  
    >-   当IAM用户的用户组的所属策略从MRS Viewer向MRS User、MRS Admin、MRS Administrator变化时，由于集群节点的sssd缓存刷新需要时间，因此同步完成后，请等待5分钟，等待新修改策略生效之后，再进行提交作业。否则，会出现提交作业失败的情况。  
    >-   当IAM用户的用户组的所属策略从MRS User、MRS Admin、MRS Administrator向MRS Viewer变化时，由于集群节点的sssd缓存刷新需要时间，因此同步完成后，请等待5分钟，新修改策略才能生效。  

4.  单击“作业管理“，进入“作业管理“页签。
5.  若集群为MRS 1.8.7、MRS 1.8.10版本或MRS 2.0.1之后版本，请单击“添加“，进入添加作业页面，“作业类型“选择“SparkSql“，作业参考[表1](#table063345817183)配置SparkSql作业信息。

    **表 1**  作业配置信息

    <a name="table063345817183"></a>
    <table><thead align="left"><tr id="row3627105831812"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p13627558111812"><a name="p13627558111812"></a><a name="p13627558111812"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="p762712581187"><a name="p762712581187"></a><a name="p762712581187"></a>参数说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row17631185817185"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p0630115810185"><a name="p0630115810185"></a><a name="p0630115810185"></a>作业名称</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p18545319122216"><a name="p18545319122216"></a><a name="p18545319122216"></a>作业名称，只能由字母、数字、中划线和下划线组成，并且长度为1～64个字符。</p>
    <div class="note" id="note163999410228"><a name="note163999410228"></a><a name="note163999410228"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0173264852_p123692397276"><a name="zh-cn_topic_0173264852_p123692397276"></a><a name="zh-cn_topic_0173264852_p123692397276"></a>建议不同的作业设置不同的名称。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row1863110583186"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p463112581183"><a name="p463112581183"></a><a name="p463112581183"></a>SQL类型</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p1663165801816"><a name="p1663165801816"></a><a name="p1663165801816"></a>SQL查询语句提交类型。</p>
    <a name="ul1563155810180"></a><a name="ul1563155810180"></a><ul id="ul1563155810180"><li>SQL</li><li>Script</li></ul>
    </td>
    </tr>
    <tr id="row66312586181"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p863175841817"><a name="p863175841817"></a><a name="p863175841817"></a><span>SQL语句</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p5631175841817"><a name="p5631175841817"></a><a name="p5631175841817"></a><span class="parmname" id="zh-cn_topic_0173264854_parmname1481912464617"><a name="zh-cn_topic_0173264854_parmname1481912464617"></a><a name="zh-cn_topic_0173264854_parmname1481912464617"></a>“SQL类型”</span>参数为<span class="parmvalue" id="zh-cn_topic_0173264854_parmvalue17647183144620"><a name="zh-cn_topic_0173264854_parmvalue17647183144620"></a><a name="zh-cn_topic_0173264854_parmvalue17647183144620"></a>“SQL”</span>时参数有效，请输入待运行的SQL语句，然后单击<span class="parmvalue" id="zh-cn_topic_0173264854_parmvalue10920547498"><a name="zh-cn_topic_0173264854_parmvalue10920547498"></a><a name="zh-cn_topic_0173264854_parmvalue10920547498"></a>“检查”</span>来检查SQL语句的正确性，确保输入语句正确。如果同时需要提交多条语句并执行，使用<span class="parmvalue" id="zh-cn_topic_0173264854_parmvalue48418579172755"><a name="zh-cn_topic_0173264854_parmvalue48418579172755"></a><a name="zh-cn_topic_0173264854_parmvalue48418579172755"></a>“;”</span>分隔不同语句。</p>
    </td>
    </tr>
    <tr id="row1063255814180"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p7631105820185"><a name="p7631105820185"></a><a name="p7631105820185"></a>SQL文件</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p3632115815183"><a name="p3632115815183"></a><a name="p3632115815183"></a><span class="parmname" id="zh-cn_topic_0173264854_parmname112719181471"><a name="zh-cn_topic_0173264854_parmname112719181471"></a><a name="zh-cn_topic_0173264854_parmname112719181471"></a>“SQL类型”</span>参数为<span class="parmvalue" id="zh-cn_topic_0173264854_parmvalue12296102615473"><a name="zh-cn_topic_0173264854_parmvalue12296102615473"></a><a name="zh-cn_topic_0173264854_parmvalue12296102615473"></a>“Script”</span>时参数有效，待执行SQL文件的路径，需要满足以下要求。</p>
    <a name="ul1375493195654"></a><a name="ul1375493195654"></a><ul id="ul1375493195654"><li>最多为1023字符，不能包含;|&amp;&gt;,&lt;'$特殊字符，且不可为空或全空格。</li><li>执行程序路径可存储于HDFS或者OBS中，不同的文件系统对应的路径存在差异。<a name="zh-cn_topic_0173264852_ul193701439132718"></a><a name="zh-cn_topic_0173264852_ul193701439132718"></a><ul id="zh-cn_topic_0173264852_ul193701439132718"><li>OBS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue53701639102718"><a name="zh-cn_topic_0173264852_parmvalue53701639102718"></a><a name="zh-cn_topic_0173264852_parmvalue53701639102718"></a>“s3a://”</span>开头。示例：s3a://wordcount/program/xxx.jar</li><li>OBS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue206061837142219"><a name="zh-cn_topic_0173264852_parmvalue206061837142219"></a><a name="zh-cn_topic_0173264852_parmvalue206061837142219"></a>“obs://”</span>开头。示例：obs://wordcount/program/xxx.jar。（MRS 2.0.5及之后版本版本支持。）</li><li>HDFS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue73701139162714"><a name="zh-cn_topic_0173264852_parmvalue73701139162714"></a><a name="zh-cn_topic_0173264852_parmvalue73701139162714"></a>“/user”</span>开头。</li></ul>
    </li><li>SparkScript和HiveScript需要以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue037073911277"><a name="zh-cn_topic_0173264852_parmvalue037073911277"></a><a name="zh-cn_topic_0173264852_parmvalue037073911277"></a>“.sql”</span>结尾，MapReduce需要以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue3370173972716"><a name="zh-cn_topic_0173264852_parmvalue3370173972716"></a><a name="zh-cn_topic_0173264852_parmvalue3370173972716"></a>“.jar”</span>结尾，Flink和SparkSubmit需要以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue0370123910279"><a name="zh-cn_topic_0173264852_parmvalue0370123910279"></a><a name="zh-cn_topic_0173264852_parmvalue0370123910279"></a>“.jar”</span>或<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue6370739122720"><a name="zh-cn_topic_0173264852_parmvalue6370739122720"></a><a name="zh-cn_topic_0173264852_parmvalue6370739122720"></a>“.py”</span>结尾。sql、jar、py不区分大小写。</li></ul>
    <div class="note" id="note120382412284"><a name="note120382412284"></a><a name="note120382412284"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0173264854_p86295129218"><a name="zh-cn_topic_0173264854_p86295129218"></a><a name="zh-cn_topic_0173264854_p86295129218"></a>MRS 2.0.5及之后版本的集群，存储在OBS上的文件路径支持以<span class="parmvalue" id="zh-cn_topic_0173264854_parmvalue662931215216"><a name="zh-cn_topic_0173264854_parmvalue662931215216"></a><a name="zh-cn_topic_0173264854_parmvalue662931215216"></a>“obs://”</span>开头格式。如需使用该格式提交作业，访问OBS需要配置对应权限。</p>
    <a name="zh-cn_topic_0173264854_ul11997202215231"></a><a name="zh-cn_topic_0173264854_ul11997202215231"></a><ul id="zh-cn_topic_0173264854_ul11997202215231"><li>创建集群时开启“OBS权限控制”功能时，可直接使用<span class="parmvalue" id="zh-cn_topic_0173264854_parmvalue3657151711249"><a name="zh-cn_topic_0173264854_parmvalue3657151711249"></a><a name="zh-cn_topic_0173264854_parmvalue3657151711249"></a>“obs://”</span>路径，无需单独配置。</li><li>创建集群时未开启或不支持（MRS 2.0.5及之后版本支持）“OBS权限控制”功能时，请参考<a href="obs方式访问OBS.md">访问OBS</a>页面进行配置。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row76331558111810"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p12633105851810"><a name="p12633105851810"></a><a name="p12633105851810"></a><span>运行程序参数</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p136331358111815"><a name="p136331358111815"></a><a name="p136331358111815"></a>为本次执行的作业配置相关优化参数（例如线程、内存、CPU核数等），用于优化资源使用效率，提升作业的执行性能。</p>
    </td>
    </tr>
    <tr id="row1633145861818"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p18633758131811"><a name="p18633758131811"></a><a name="p18633758131811"></a>服务配置参数</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p0595819249"><a name="p0595819249"></a><a name="p0595819249"></a>可选参数，用于为本次执行的作业修改服务配置参数。该参数的修改仅适用于本次执行的作业，如需对集群永久生效，请参考<a href="配置服务参数.md">配置服务参数</a>页面进行修改。</p>
    <p id="p1793619348256"><a name="p1793619348256"></a><a name="p1793619348256"></a>如需添加多个参数，请单击右侧<a name="zh-cn_topic_0173264852_image137133942711"></a><a name="zh-cn_topic_0173264852_image137133942711"></a><span><img id="zh-cn_topic_0173264852_image137133942711" src="figures/zh-cn_image_0183017691.png"></span>增加，如需删除参数，请单击右侧<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue163711139122718"><a name="zh-cn_topic_0173264852_parmvalue163711139122718"></a><a name="zh-cn_topic_0173264852_parmvalue163711139122718"></a>“删除”</span>。</p>
    </td>
    </tr>
    <tr id="row16633145871815"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="p136331582189"><a name="p136331582189"></a><a name="p136331582189"></a>命令参考</p>
    </td>
    <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="p204063412410"><a name="p204063412410"></a><a name="p204063412410"></a>用于展示提交作业时提交到后台执行的命令。</p>
    </td>
    </tr>
    </tbody>
    </table>

6.  若集群为MRS 1.8.7之前版本或者MRS 2.0.1版本，按照如下方法添加Spark Script作业和Spark SQL作业。
    -   Spark Script作业：在作业页签单击“添加“进入添加作业页面，“作业类型“选择“Spark Script“，请参考[表2](#table1444481515202)配置作业信息。
    -   Spark SQL作业：选择Spark SQL页签，添加SQL语句，然后检查并提交SQL语句。

        **表 2**  作业配置信息

        <a name="table1444481515202"></a>
        <table><thead align="left"><tr id="zh-cn_topic_0173264852_rfd2a08fd0ba94517ba01e4ded7454cac"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0173264852_af11d9c3dce6c499d8eec0a138b99d392"><a name="zh-cn_topic_0173264852_af11d9c3dce6c499d8eec0a138b99d392"></a><a name="zh-cn_topic_0173264852_af11d9c3dce6c499d8eec0a138b99d392"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0173264852_ab83f3f06c8cc46369dd5073ae93c3b97"><a name="zh-cn_topic_0173264852_ab83f3f06c8cc46369dd5073ae93c3b97"></a><a name="zh-cn_topic_0173264852_ab83f3f06c8cc46369dd5073ae93c3b97"></a>参数说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="zh-cn_topic_0173264852_row16309131791918"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0173264852_p1931011715198"><a name="zh-cn_topic_0173264852_p1931011715198"></a><a name="zh-cn_topic_0173264852_p1931011715198"></a>作业名称</p>
        </td>
        <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0173264852_p1267051812192"><a name="zh-cn_topic_0173264852_p1267051812192"></a><a name="zh-cn_topic_0173264852_p1267051812192"></a>作业名称，只能由字母、数字、中划线和下划线组成，并且长度为1～64个字符。</p>
        <div class="note" id="zh-cn_topic_0173264852_note067018184197"><a name="zh-cn_topic_0173264852_note067018184197"></a><a name="zh-cn_topic_0173264852_note067018184197"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0173264852_p1167017186195"><a name="zh-cn_topic_0173264852_p1167017186195"></a><a name="zh-cn_topic_0173264852_p1167017186195"></a>建议不同的作业设置不同的名称。</p>
        </div></div>
        </td>
        </tr>
        <tr id="zh-cn_topic_0173264852_rbd79ceb2feb141ff9cb37ffde9e08ed7"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0173264852_a4e9842e891a449118c2e3811caa071d9"><a name="zh-cn_topic_0173264852_a4e9842e891a449118c2e3811caa071d9"></a><a name="zh-cn_topic_0173264852_a4e9842e891a449118c2e3811caa071d9"></a>执行程序路径</p>
        </td>
        <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0173264852_p655627719565"><a name="zh-cn_topic_0173264852_p655627719565"></a><a name="zh-cn_topic_0173264852_p655627719565"></a>待执行程序包地址，需要满足如下要求：</p>
        <a name="zh-cn_topic_0173264852_ul1375493195654"></a><a name="zh-cn_topic_0173264852_ul1375493195654"></a><ul id="zh-cn_topic_0173264852_ul1375493195654"><li>最多为1023字符，不能包含;|&amp;&gt;,&lt;'$特殊字符，且不可为空或全空格。</li><li>执行程序路径可存储于HDFS或者OBS中，不同的文件系统对应的路径存在差异。<a name="zh-cn_topic_0173264852_ul56833471484"></a><a name="zh-cn_topic_0173264852_ul56833471484"></a><ul id="zh-cn_topic_0173264852_ul56833471484"><li>OBS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue15615586113316"><a name="zh-cn_topic_0173264852_parmvalue15615586113316"></a><a name="zh-cn_topic_0173264852_parmvalue15615586113316"></a>“s3a://”</span>开头。示例：s3a://wordcount/program/xxx.jar</li><li>HDFS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue5002226915745"><a name="zh-cn_topic_0173264852_parmvalue5002226915745"></a><a name="zh-cn_topic_0173264852_parmvalue5002226915745"></a>“/user”</span>开头。</li></ul>
        </li><li>Spark Script需要以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue3709601695914"><a name="zh-cn_topic_0173264852_parmvalue3709601695914"></a><a name="zh-cn_topic_0173264852_parmvalue3709601695914"></a>“.sql”</span>结尾，MR和Spark需要以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue940908595918"><a name="zh-cn_topic_0173264852_parmvalue940908595918"></a><a name="zh-cn_topic_0173264852_parmvalue940908595918"></a>“.jar”</span>结尾。sql、jar不区分大小写。</li></ul>
        </td>
        </tr>
        <tr id="zh-cn_topic_0173264852_r7dcde55c00da4bc88afb2b022bce0abd"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0173264852_a61afb54329564e458086d7622bda3b89"><a name="zh-cn_topic_0173264852_a61afb54329564e458086d7622bda3b89"></a><a name="zh-cn_topic_0173264852_a61afb54329564e458086d7622bda3b89"></a>执行程序参数</p>
        </td>
        <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0173264852_ad6f1110b8e38456193949182f7a05980"><a name="zh-cn_topic_0173264852_ad6f1110b8e38456193949182f7a05980"></a><a name="zh-cn_topic_0173264852_ad6f1110b8e38456193949182f7a05980"></a>程序执行的关键参数，该参数由用户程序内的函数指定，MRS只负责参数的传入。多个参数间使用空格隔开。</p>
        <p id="zh-cn_topic_0173264852_p163988156203"><a name="zh-cn_topic_0173264852_p163988156203"></a><a name="zh-cn_topic_0173264852_p163988156203"></a><span>配置方法：包名.类名</span></p>
        <p id="zh-cn_topic_0173264852_a6c44712b37c74651afe354f3cbf9e02f"><a name="zh-cn_topic_0173264852_a6c44712b37c74651afe354f3cbf9e02f"></a><a name="zh-cn_topic_0173264852_a6c44712b37c74651afe354f3cbf9e02f"></a>最多为2047字符，不能包含;|&amp;&gt;&lt;'$特殊字符，可为空。</p>
        <div class="note" id="zh-cn_topic_0173264852_note62371709174814"><a name="zh-cn_topic_0173264852_note62371709174814"></a><a name="zh-cn_topic_0173264852_note62371709174814"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0173264852_p20521095174814"><a name="zh-cn_topic_0173264852_p20521095174814"></a><a name="zh-cn_topic_0173264852_p20521095174814"></a>用户输入带有敏感信息（如登录密码）的参数时，可通过在参数名前添加“@”的方式，为该参数值加密，以防止敏感信息被明文形式持久化。在MRS管理控制台查看作业信息时，敏感信息显示为“*”。</p>
        <p id="zh-cn_topic_0173264852_p1265001117571"><a name="zh-cn_topic_0173264852_p1265001117571"></a><a name="zh-cn_topic_0173264852_p1265001117571"></a>例如：username=admin @password=admin_123</p>
        </div></div>
        </td>
        </tr>
        <tr id="zh-cn_topic_0173264852_r3bdfdc9102e8416492da92bb5912306e"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0173264852_a93b1caabf748429b887fe55580d1db95"><a name="zh-cn_topic_0173264852_a93b1caabf748429b887fe55580d1db95"></a><a name="zh-cn_topic_0173264852_a93b1caabf748429b887fe55580d1db95"></a>数据输入路径</p>
        </td>
        <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0173264852_a52221b5791d44544af1d6daf2bb57612"><a name="zh-cn_topic_0173264852_a52221b5791d44544af1d6daf2bb57612"></a><a name="zh-cn_topic_0173264852_a52221b5791d44544af1d6daf2bb57612"></a>数据输入地址。</p>
        <div class="p" id="zh-cn_topic_0173264852_p6028322915823"><a name="zh-cn_topic_0173264852_p6028322915823"></a><a name="zh-cn_topic_0173264852_p6028322915823"></a>数据可存储于HDFS或者OBS中，不同的文件系统对应的路径存在差异。<a name="zh-cn_topic_0173264852_ul1668690715439"></a><a name="zh-cn_topic_0173264852_ul1668690715439"></a><ul id="zh-cn_topic_0173264852_ul1668690715439"><li>OBS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue1805090015439"><a name="zh-cn_topic_0173264852_parmvalue1805090015439"></a><a name="zh-cn_topic_0173264852_parmvalue1805090015439"></a>“s3a://”</span>开头。</li><li>HDFS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue2499739115713"><a name="zh-cn_topic_0173264852_parmvalue2499739115713"></a><a name="zh-cn_topic_0173264852_parmvalue2499739115713"></a>“/user”</span>开头。</li></ul>
        </div>
        <p id="zh-cn_topic_0173264852_a8c411087de5a4952a0a0763536c2fd4a"><a name="zh-cn_topic_0173264852_a8c411087de5a4952a0a0763536c2fd4a"></a><a name="zh-cn_topic_0173264852_a8c411087de5a4952a0a0763536c2fd4a"></a>最多为1023字符，不能包含;|&amp;&gt;,&lt;'$特殊字符，可为空。</p>
        </td>
        </tr>
        <tr id="zh-cn_topic_0173264852_r26ccf29d38884d09b5b2c445f49e3f0a"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p752552114273"><a name="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p752552114273"></a><a name="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p752552114273"></a>输出路径</p>
        </td>
        <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0173264852_af95377875ef1449db585f0d23bdc5096"><a name="zh-cn_topic_0173264852_af95377875ef1449db585f0d23bdc5096"></a><a name="zh-cn_topic_0173264852_af95377875ef1449db585f0d23bdc5096"></a>数据输出地址。</p>
        <div class="note" id="zh-cn_topic_0173264852_note12918618161337"><a name="zh-cn_topic_0173264852_note12918618161337"></a><a name="zh-cn_topic_0173264852_note12918618161337"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0173264852_ul1637410244522"></a><a name="zh-cn_topic_0173264852_ul1637410244522"></a><ul id="zh-cn_topic_0173264852_ul1637410244522"><li>配置此参数时，单击<span class="uicontrol" id="zh-cn_topic_0173264852_uicontrol23741024125214"><a name="zh-cn_topic_0173264852_uicontrol23741024125214"></a><a name="zh-cn_topic_0173264852_uicontrol23741024125214"></a>“OBS”</span>或<span class="uicontrol" id="zh-cn_topic_0173264852_uicontrol17374112412529"><a name="zh-cn_topic_0173264852_uicontrol17374112412529"></a><a name="zh-cn_topic_0173264852_uicontrol17374112412529"></a>“HDFS”</span>，并选择文件目录，或者手动输入文件目录，然后单击<span class="uicontrol" id="zh-cn_topic_0173264852_uicontrol43744241528"><a name="zh-cn_topic_0173264852_uicontrol43744241528"></a><a name="zh-cn_topic_0173264852_uicontrol43744241528"></a>“确定”</span>。</li><li>若添加hadoop-mapreduce-examples-x.x.x.jar样例程序或和hadoop-mapreduce-examples-x.x.x.jar类似的程序，请手动输入一个不存在的目录。</li></ul>
        </div></div>
        <div class="p" id="zh-cn_topic_0173264852_p60582415151053"><a name="zh-cn_topic_0173264852_p60582415151053"></a><a name="zh-cn_topic_0173264852_p60582415151053"></a>数据可存储于HDFS或者OBS中，不同的文件系统对应的路径存在差异。<a name="zh-cn_topic_0173264852_ul8370831151053"></a><a name="zh-cn_topic_0173264852_ul8370831151053"></a><ul id="zh-cn_topic_0173264852_ul8370831151053"><li>OBS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue6948719151053"><a name="zh-cn_topic_0173264852_parmvalue6948719151053"></a><a name="zh-cn_topic_0173264852_parmvalue6948719151053"></a>“s3a://”</span>开头。</li><li>HDFS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue32451534151053"><a name="zh-cn_topic_0173264852_parmvalue32451534151053"></a><a name="zh-cn_topic_0173264852_parmvalue32451534151053"></a>“/user”</span>开头。</li></ul>
        </div>
        <p id="zh-cn_topic_0173264852_aece1cf44e4734f94b3196ff9e9bf38e8"><a name="zh-cn_topic_0173264852_aece1cf44e4734f94b3196ff9e9bf38e8"></a><a name="zh-cn_topic_0173264852_aece1cf44e4734f94b3196ff9e9bf38e8"></a>最多为1023字符，不能包含;|&amp;&gt;,&lt;'$特殊字符，可为空。</p>
        </td>
        </tr>
        <tr id="zh-cn_topic_0173264852_rff1753bde96f4e81a0631197ac349003"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p287101489174"><a name="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p287101489174"></a><a name="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p287101489174"></a>日志路径</p>
        </td>
        <td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0173264852_a2bcc88a179f346448d93d0da091aa47f"><a name="zh-cn_topic_0173264852_a2bcc88a179f346448d93d0da091aa47f"></a><a name="zh-cn_topic_0173264852_a2bcc88a179f346448d93d0da091aa47f"></a>作业日志存储地址，该日志信息记录作业运行状态。</p>
        <div class="p" id="zh-cn_topic_0173264852_p52515849151155"><a name="zh-cn_topic_0173264852_p52515849151155"></a><a name="zh-cn_topic_0173264852_p52515849151155"></a>数据可存储于HDFS或者OBS中，不同的文件系统对应的路径存在差异。<a name="zh-cn_topic_0173264852_ul2880601151155"></a><a name="zh-cn_topic_0173264852_ul2880601151155"></a><ul id="zh-cn_topic_0173264852_ul2880601151155"><li>OBS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue32002114151155"><a name="zh-cn_topic_0173264852_parmvalue32002114151155"></a><a name="zh-cn_topic_0173264852_parmvalue32002114151155"></a>“s3a://”</span>开头。</li><li>HDFS：以<span class="parmvalue" id="zh-cn_topic_0173264852_parmvalue42765641151155"><a name="zh-cn_topic_0173264852_parmvalue42765641151155"></a><a name="zh-cn_topic_0173264852_parmvalue42765641151155"></a>“/user”</span>开头。</li></ul>
        </div>
        <p id="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p438206609174"><a name="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p438206609174"></a><a name="zh-cn_topic_0173264852_zh-cn_topic_0012807343_p438206609174"></a>最多为1023字符，不能包含;|&amp;&gt;,&lt;'$特殊字符，可为空。</p>
        </td>
        </tr>
        </tbody>
        </table>

7.  确认作业配置信息，单击“确定“，完成作业的新增。

    作业新增完成后，可对作业进行管理。


