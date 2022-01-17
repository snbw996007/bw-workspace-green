# MySQL常见问题

**远程连接报错**

输入mysql -hxxx.xxx.xxx.xxx -uroot -pxxx后提示

ERROR 1130 (HY000): Host '10.2.223.11' is not allowed to connect to this MySQL server

解决方法

mysql>use mysql;
mysql>update user set host = '%' where user = 'root';
mysql>flush privileges;
mysql>select host, user from user;
mysql>quit
重启mysql服务
