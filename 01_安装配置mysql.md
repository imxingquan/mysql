##Linux 安装配置mysql  

```
$ sudo apt-get install mysql-server
``` 
安装路径   
```
/usr/bin                 客户端程序和脚本
/usr/sbin                mysqld 服务器    
/var/lib/mysql           日志文件，数据库    
/usr/share/doc/packages  文档    
/usr/include/mysql       包含( 头) 文件    
/usr/lib/mysql           库    
/usr/share/mysql         错误消息和字符集文件    
/usr/share/sql-bench     基准程序   
```
##修改查看端口

```
$ netstat -an | grep 3306
```

##修改配置文件

```
$ sudo vim /etc/mysql/mysql.conf.d/mysqld.cnf
```
使用#注释掉以下行
```
bind-address          = 127.0.0.1
```

##重启mysql

```
$ sudo service mysql restart
```
##配置root用户可以远程登录

```mysql
mysql>GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123' WITH GRANT OPTION;
mysql>flush privileges;
```

经过以上步骤就可以从windows访问到虚拟机的mysql了,如果防火墙有阻挡3306端口请注意关闭.

##参考  

Mysql初始化root密码和允许远程访问 http://www.cnblogs.com/cnblogsfans/archive/2009/09/21/1570942.html 
压缩包安装mysql https://jingyan.baidu.com/article/a378c9609eb652b3282830fd.html   
Virtualbox怎么设置访问外网以及主机访问虚拟机 https://jingyan.baidu.com/article/948f592410a763d80ef5f910.html 


