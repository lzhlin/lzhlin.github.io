---
title: The server time zone value???
categories: Mysql
tags: Mysql
comments: true
date: 2018-11-24 23:01:16
---

Java项目连接数据库报时区错误

The server time zone value '???ú±ê×??±??'

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/The%20server%20time%20zone%20value/mysql%E6%97%B6%E5%8C%BA.png)



解决方案：

为URL添加参数**serverTimezone=UTC**即可，这里的时区可以根据自己数据库的设定来设置（GMT/UTC ）。

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/The%20server%20time%20zone%20value/mysql%E9%85%8D%E7%BD%AE.png)



