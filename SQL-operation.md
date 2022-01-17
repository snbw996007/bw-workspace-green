# 数据库相关（key:value）

**数据库类型：MySQL Mariadb Oracle db2 SQL Server Sybase**

**数据库类型：NoSQL MongoDB Redis**

# MySQL--SQL语句

**DDL:数据定义语言，定义数据库/表结构**

create，drop，alter

**DML:数据操纵语言**

insert，update，delete

**DCL:数据控制语言，权限，安全设置**

grant

**DQL:数组查询语言**

select，from，where

**远程登录MySQL服务器**

mysql -hxxx.xxx.xxx.xxx -uroot -pxxx

# 数据库基础操作

**创建数据库**

create database xxx character set x(指定字符集) collate x(核对规则);

**查看数据库（定义）**

show databases;
show create database x;

**修改数据库**

alter database xxx character set x;

**删除数据库**

drop database xxx;

**切换数据库**

use xxx;

**查看当前使用库**

select database();

# 表操作

**创建表**

create table 表名(列名 列类型(L字符个数) 约束 ...);

列类型：int char(固定)/varchar(可变) double float text(文本) blob(二进制) date time datetime(NULL) timestamp(时间戳，默认当前时间)

列约束：primary key,unique,not null

**查看表（定义）**

show tables;
show create table x;

**查看表结构**

desc xxx;

**修改表**

添加列add--alter table xxx add 列名 列类型 约束;

修改列modify--alter table xxx modify 列名 列类型;

修改列名change--alter table xxx change 列名 列新名 列类型;

删除drop--alter table xxx drop 列名;

**修改表名**

rename table xxx to xxx;

**修改表字符集**

alter table xxx charater set 字符集;

**删除表**

drop table xxx;

