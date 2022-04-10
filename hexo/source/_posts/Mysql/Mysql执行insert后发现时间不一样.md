---
title: Mysql执行insert后发现时间不一样
categories: Mysql
tags: Mysql
comments: true
date: 2018-12-20 01:43:14
---

在项目中执行插入之后发现添到数据库中的时间与实际不一样

例如 我 insert into table (uid,create_time) values('a','2018-12-20 01:45:00:000')

执行完毕后,数据库中发现该记录中的create_time值为2018-12-19 17:15:00:000

所有插入的数据都提前了八个小时,并且传入的值确实是2018-12-20 01:45:00:000没错

<!-- more -->

原因:

链接数据库时数据库的配置是:

`db.url=jdbc:mysql://127.0.0.1:3306/let_ticket?useUnicode=true&amp&characterEncoding=utf-8&autoReconnect=true&serverTimezone=UTC&useSSL=false`

关键就是在serverTimezone=UTC上面,改为CTT即可 （Asia&Shanghai）



UTC：

    先看下百度百科上给出的定义：
    
        协调世界时，又称世界统一时间，世界标准时间，国际协调时间。它是以原子时秒长为基础，在时刻上尽量接近于世界时的一种时间计量系统。

GMT：

        格林尼治平太阳时间，是指在格林尼治所在地的标准时间。以地球自转为基础的时间计量系统。

相对来说，UTC的计算过程相当严谨精密，因此若以「世界标准时间」的角度来说，UTC比GMT来得更加精准。

其误差值必须保持在0.9秒以内，若大于0.9秒则由位于巴黎的国际地球自转事务中央局发布闰秒，使UTC与地球自转周期一致。

所以基本上UTC的本质强调的是比GMT更为精确的世界时间标准.它其实是个更精确的GMT.

        和北京时间的转换关系：加上时区即可，比如北京在东八区。
    
        北京时间=UTC+8=GMT+8
---------------------
最后是这样的:

`db.url=jdbc:mysql://127.0.0.1:3306/let_ticket?useUnicode=true&amp&characterEncoding=utf-8&autoReconnect=true&serverTimezone=CTT&useSSL=false`