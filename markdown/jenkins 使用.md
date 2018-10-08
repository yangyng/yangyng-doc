## Jenkins windows 使用 ##
#### 下载地址 ####
 
[https://jenkins.io/download/](https://jenkins.io/download/ "Jenkins 下载地址")
#### 修改端口号 默认端口号 8080 ####
 
**文件所在安装路径 -> 范例 D:\tool\jenkins\jenkins.xml**

    <arguments>-Xrs -Xmx256m -Dhudson.lifecycle=hudson.lifecycle.WindowsServiceLifecycle -jar "%BASE%\jenkins.war" --httpPort=8080 --webroot="%BASE%\war"</arguments>







