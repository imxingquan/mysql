## MySQL windows下免安装版配置

### 安装到windows服务的脚本 
···
cd bin
mysqld install mysql --defaults-file=D:\soft\mysql57\my.ini
net start mysql
···

### 移除服务脚本 
···
net stop mysql
bin\mysqld --remove mysql
···

### 独立运行的脚本  
cd bin
mysqld.exe  --defaults-file=../my.ini --console


如果使用安装服务的脚本my.ini配置中的相关路径要用绝对地址
