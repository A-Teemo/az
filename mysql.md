## 安装mysql
```
1.安装mysql
sudo apt install mysql-server
２．测试有没有装,进入mysql
mysql -uroot -p
３．更改mysql编码改成utf-8
停止mysql服务：sudo service mysql stop
查看mysql服务状态：sudo service mysql status
４．修改mysql配置文件
目录：/etc/mysql/my.cnf
sudo nano my.cnf

添加一下内容：
[client]
default-character-set = utf8

[mysqld]
character-set-server = utf8
collation-server = utf8_general_ci
bind-address = 0.0.0.0

5.查看是否修改成功
启动mysql服务:sudo service mysql start
进入mysql:mysql -uroot -p

查看编码：
show variables like '%char%';
shwo variables like '%colla%';
```
