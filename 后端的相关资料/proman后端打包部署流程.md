# Proman 后端打包部署流程


打包前:

1.配置yml文件 正式服prod或者测试服dev

2.修改src/main/java/com/pantech/boot/module/aviationstandards/controller/StandardsController.java中
/preview 
的url地址，测试服为String url = "http://10.1.16.18:8088/aviation_standards/preview2?id=" + standardsId;
正式服为：String url = "http://10.1.16.214:8088/aviation_standards/preview2?id=" + standardsId;
---

ip：10.1.16.18

用户名：root

密码：123abc,



## 1. 工具

XShell+XFtp

## 2. 目录

../usr/local/boot/

## 3. 命令

1. 关闭原有服务

    ps -ef|grep java （找到服务的进程号）

    ![image-20201112100216904](/proman后端打包部署流程.assets/image-20201112100216904.png)

    kill -9 XXX(进程号)

2. 启动新服务

    nohup java -jar proman20201112.jar > proman.log 2>&1 &





部署完后mapper文件还原（到mapper文件夹trunk\src\proman\src\main\resources\mapper，右键TortoiseSVN-》revert-》打钩select-》取消打钩clear Changelist）