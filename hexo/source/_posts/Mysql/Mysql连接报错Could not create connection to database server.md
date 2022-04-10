---
title: Mysql连接报错Could not create connection to database server
categories: Mysql
tags: Mysql
comments: true
date: 2018-11-24 22:48:39
---

Java项目访问数据库报错

`Could not create connection to database server. Attempted reconnect 3 times. Giving up.`

尝试连接了三次,最后放弃

<!-- more -->

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E8%BF%9E%E6%8E%A5%E6%8A%A5%E9%94%99Could%20not%20create%20connection%20to%20database%20server/mysql.png)

一开始可能认为是配置的错误,后来发现不是

本地数据库用的是Mysql8.0的版本,而数据库连接驱动mysql-connector-java是5.7的

去maven仓库升级jar的版本后就好了