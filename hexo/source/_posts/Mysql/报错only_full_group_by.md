---
title: 报错only_full_group_by
categories: Mysql
tags: Mysql
comments: true
date: 2018-11-26 00:50:24

---

报错如下:

`Expression #1 of SELECT list is not in GROUP BY clause and contains nonaggregated column 't.line_name' which is not functionally dependent on columns in GROUP BY clause; this is incompatible with sql_mode=only_full_group_by`

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/%E6%8A%A5%E9%94%99only-full-group-by/%E6%8A%A5%E9%94%99.png)



原因:

MySQL 5.7.5及以上功能依赖检测功能。如果启用了ONLY_FULL_GROUP_BY SQL模式（默认情况下），MySQL将拒绝选择列表，HAVING条件或ORDER BY列表的查询引用在GROUP BY子句中既未命名的非集合列，也不在功能上依赖于它们。（5.7.5之前，MySQL没有检测到功能依赖关系，默认情况下不启用ONLY_FULL_GROUP_BY)



解决:

先查询一下sql_mode

`select @@global.sql_mode`

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/%E6%8A%A5%E9%94%99only-full-group-by/select.png)

它的值为 `ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION`



去掉 `ONLY_FULL_GROUP_BY`,重新设值

`set @@global.sql_mode 
='STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION'`



![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/%E6%8A%A5%E9%94%99only-full-group-by/ok.png)

然后报错就没有了



2018.12.20 1:30更新:

数据库服务重启之后,又会出现此错误

解决方式:

在配置文件中mysqld里面加入:

`sql_mode=STRICT_TRANS_TABLES,NO_ZERO_IN_DATE,NO_ZERO_DATE,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION`

例如,我的是windows版本的数据库, 在my.ini中加入

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/%E6%8A%A5%E9%94%99only-full-group-by/sqlMode%E9%85%8D%E7%BD%AE.png)

重启服务后就好了.