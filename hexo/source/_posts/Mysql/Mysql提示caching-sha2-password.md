---
title: Mysql提示caching_sha2_password
categories: Mysql
tags: Mysql
comments: true
date: 2018-11-24 21:40:21
---

在下载新的Mysql8.0安装完成后,通过Navicat、sqlyog、或者程序中连接数据库时，提示：`Authentication plugin 'caching_sha2_password' cannot be loaded` 的错误

mysql 8.0 默认使用 caching_sha2_password 身份验证机制 —— 从原来的 mysql_native_password 更改为 caching_sha2_password。 
从 5.7 升级 8.0 版本的不会改变现有用户的身份验证方法，但新用户会默认使用新的 caching_sha2_password 。

<!-- more -->

解决方案:

修改用户的密码和加密方式

1.使用cmd命令框进入mysql的bin目录,登录mysql

输入密码时,刚安装完成的用户密码可能为空,直接回车即可

`C:\Users\LinPP>E:`

` E:\>cd E:\mysql-8.0.11-winx64\bin`

`E:\mysql-8.0.11-winx64\bin>mysql -u root -p`

`Enter password:`

`mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '123456';`

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E6%8F%90%E7%A4%BAcaching_sha2_password/cmd.png)

如图,修改了加密方式,并且将密码改为123456,之后即可连接



虽然那几种连接工具能用了 今天使用一款工具发现又出现了同样的问题

解决方案:

Mysql根目录下寻找配置文件 my.ini

若不存在 ,可自行创建

内容:

```
[mysqld]
# 设置3306端口
port=3306
# 允许最大连接数
max_connections=200
# 允许连接失败的次数。这是为了防止有人从该主机试图攻击数据库系统
max_connect_errors=10
# 服务端使用的字符集默认为UTF8
character-set-server=utf8
# 创建新表时将使用的默认存储引擎
default-storage-engine=INNODB
# 默认使用“mysql_native_password”插件认证
default_authentication_plugin=mysql_native_password
[mysql]
# 设置mysql客户端默认字符集
default-character-set=utf8
[client]
# 设置mysql客户端连接服务端时默认使用的端口
port=3306
default-character-set=utf8
```



主要是这句

`default_authentication_plugin=mysql_native_password`

将Mysql的默认加密方式更改为mysql_native_password

之后即可连接