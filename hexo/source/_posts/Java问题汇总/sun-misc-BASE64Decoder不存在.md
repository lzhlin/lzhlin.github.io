---
title: sun.misc.BASE64Decoder不存在
categories: Java问题汇总
tags: Java
comments: true
date: 2018-11-24 22:09:27
---

公司的项目在家里打开以后发现两个类报错

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Java%E9%97%AE%E9%A2%98%E6%B1%87%E6%80%BB/sun-misc-BASE64Decoder%E4%B8%8D%E5%AD%98%E5%9C%A8/base64.png)

<!-- more -->

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Java%E9%97%AE%E9%A2%98%E6%B1%87%E6%80%BB/sun-misc-BASE64Decoder%E4%B8%8D%E5%AD%98%E5%9C%A8/regexp.png)



查询资料后发现,JDK中的lib\tools.jar和JRE中的lib\rt.jar已从Java SE 9中删除。这些JAR中可用的类和资源现在以文件中的内部格式存储在lib目录的命名模块中。 可以使用称为jrt的新方案来从运行时映像检索这些类和资源。 依靠这些JAR位置的应用程序将不再工作。

而我家里用的JDK10, 把项目JDK环境换成1.8的版本,就解决了

