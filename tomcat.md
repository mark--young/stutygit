> jdk安装 集成开发工具 eclipse 






> C:\Windows\System32\drivers\etc\hosts  

127.0.0.1 example.com 不能有星号

如果不能访问 127.0.0.1 把IP6给去掉.点属性.


1
```
<Connector port="8080" protocol="HTTP/1.1"
               connectionTimeout="20000"
               redirectPort="8443" />
```
**改为**
> 
```
<Connector port="8080" protocol="HTTP/1.1"
               connectionTimeout="20000"
               redirectPort="8443" />
               

```


2
```

 <Host appBase="webapps" autoDeploy="true" name="localhost" unpackWARs="true" xmlNamespaceAware="false" xmlValidation="false"> 
 </host>

```
改为

```
<Host appBase="webapps" autoDeploy="true" name="hr.xinyanyuan.com.cn" unpackWARs="true" xmlNamespaceAware="false" xmlValidation="false">  
```
<Context docBase="hr" path="" reloadable="true" />

3

```
 <Engine name="Catalina" defaultHost="localhost">
 ```
改为

```
 <Engine name="Catalina" defaultHost="hr.xinyanyuan.com.cn">
```




较为完整tomcat介绍版本:
```
http://blog.csdn.net/xiaokui_wingfly/article/details/46665681
```

> 在 Windows 防火墙中打开端口
打开端口 80
在 “开始” 菜单上单击 “控制面板”，单击 “系统和安全”，然后单击 “Windows 防火墙”。 不为“类别”视图配置控制面板，您只需要选择 “Windows 防火墙”。
单击 “高级设置”。
单击 “入站规则”。
在 “操作” 窗口中单击 “新建规则” 。
单击 “端口” 的 “规则类型”。
单击“下一步” 。
在 “协议和端口” 页上，单击 TCP。
选择 “特定本地端口” ，然后键入值 80。
单击“下一步” 。
在 “操作” 页上，单击 “允许连接”。
单击“下一步” 。
在 “配置文件” 页上，单击适合您的环境的选项。
单击“下一步” 。
在 名称 页上，输入的名称为ReportServer (TCP 端口 80 上)
单击 “完成”。
重新启动计算机。

**乱码问题/移动端乱码问题**
```
<Connector port="8080"protocol="HTTP/1.1"
connectionTimeout="20000"
redirectPort="8443"URIEncoding="UTF-8" />
```

```
〈meta http-equiv="Content-Type" content="text/html; charset=utf-8">
```

> 保持文件也是utf-8的格式.还有一个办法是打开文件之后点击菜单File——>Save as，在弹出的对话框的最下面就是当前文件的编码，更改编码之后保存并覆盖原文件就相当于修改了此文件的编码。
