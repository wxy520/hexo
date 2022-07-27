# shell脚本开机自启

### 1.将(脚本)启动文件移动到 /etc/init.d/或者/etc/rc.d/init.d/目录下。（前者是后者的软连接）
```bash
mv  /www/wwwroot/test.sh /etc/rc.d/init.d
```


### 2.启动文件前面务必添加如下三行代码，否侧会提示chkconfig不支持。
#!/bin/sh                          告诉系统使用的shell,所以的shell脚本都是这样
#chkconfig: 35 20 80               分别代表运行级别，启动优先权，关闭优先权，此行代码必须
#description: http server          自己随便发挥！！！，此行代码必须
/bin/echo $(/bin/date +%F_%T) >> /tmp/test.log
### 3.增加脚本的可执行权限
```bash
chmod +x  /etc/rc.d/init.d/test.sh
```


### 4.添加脚本到开机自动启动项目中。添加到chkconfig，开机自启动。
```bash
[root@localhost ~]# cd /etc/rc.d/init.d
[root@localhost ~]# chkconfig --add test.sh
[root@localhost ~]# chkconfig test.sh on
```



### 5.关闭开机启动 
```bash
[root@localhost ~]# chkconfig test.sh off
```


### 6.从chkconfig管理中删除test.sh
```bash
[root@localhost ~]# chkconfig --del test.sh
```


### 7.查看chkconfig管理
```bash
[root@localhost ~]# chkconfig --list test.sh
```

