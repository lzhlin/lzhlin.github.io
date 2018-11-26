---
title: Mysql导出数据库设计文档
categories: Mysql
tags: Mysql
comments: true
date: 2018-11-25 10:53:35
---



# 方式一 DBExportDoc

在word中,利用ODBC驱动源,OFFICE宏来控制报表输出

作者博客地址: 

[https://blog.csdn.net/yzsind](https://blog.csdn.net/yzsind)



## 下载工具

工具下载:

链接：

[https://pan.baidu.com/s/1y1bERGvKM2oftkY_M5zBVg](https://pan.baidu.com/s/1y1bERGvKM2oftkY_M5zBVg)

提取码：mhtd

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/ODBC%E4%B8%8B%E8%BD%BD.png)

根据Mysql数据库的版本下载想用的驱动源

也可去官网下载:

[https://dev.mysql.com/downloads/connector/odbc/](https://dev.mysql.com/downloads/connector/odbc/)



## 双击安装ODBC

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E5%AE%89%E8%A3%85ODBC.png)



## 打开windows控制面板



打开windows控制面板,管理工具,打开ODBC64(请根据版本自行选择)



![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E6%8E%A7%E5%88%B6%E9%9D%A2%E6%9D%BF.png)



![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E7%AE%A1%E7%90%86%E5%B7%A5%E5%85%B7.png)



## 添加ODBC数据源

点击添加,选择相应版本的Mysql ODBC,点击完成,会出现连接选项

![创建数据源](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E5%88%9B%E5%BB%BA%E6%95%B0%E6%8D%AE%E6%BA%90.png)



> 第二步安装成功之后会出现相应的ODBC
>
> 8.0版本的会出现两个,一个是 ANSI driver  和 Unicode driver   两个版本。  
>
> Unicode driver  版本提供了更多字符集的支持，也就是提供了多语言的支持。而ANSI driver  版本是只针对有限的字符集的范围。



这里以添加8.0Unicode driver为例

数据源名称起名为mysql8

![数据源配置](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E8%BF%9E%E6%8E%A5%E9%85%8D%E7%BD%AE.png)



## 打开word选项,设置宏

![启用所有宏](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E5%90%AF%E7%94%A8%E6%89%80%E6%9C%89%E5%AE%8F.png)



## word连接数据源

解压压缩包,打开DBExportDoc V1.0 For MySQL.doc

连接数据库,修改相应的用户名密码以及数据源名称

![解压](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E8%A7%A3%E5%8E%8B.png)



![连接数据库](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E8%BF%9E%E6%8E%A5%E6%95%B0%E6%8D%AE%E5%BA%93.png)



![修改数据源](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E4%BF%AE%E6%94%B9%E6%95%B0%E6%8D%AE%E6%BA%90.png)

![连接成功](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E8%BF%9E%E6%8E%A5%E6%88%90%E5%8A%9F.png)



## 导出数据库表结构



选择相应的表,并导出



![选择表导出](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E9%80%89%E6%8B%A9%E8%A1%A8.png)



![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E6%96%87%E6%A1%A3.png)



> 第一次尝试就最后导出的一步一直报错,命令无效
>
> 后来重启了电脑又好了,此错不知何因





# 方式二 动软代码生成工具


动软官网: [http://www.maticsoft.com/download.aspx](http://www.maticsoft.com/download.aspx)



## 下载动软代码生成工具并解压安装

网盘下载地址:

链接：[https://pan.baidu.com/s/1gLDCjofc9-IV3g_9raan6g](https://pan.baidu.com/s/1gLDCjofc9-IV3g_9raan6g)

提取码：09hq 


解压后运行Codematic2.msi安装,安装成功后,桌面出现

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/codematic2.png)

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E5%8A%A8%E8%BD%AF%E5%9B%BE%E6%A0%87.png)

## 运行动软代码生成器

选择新增数据库服务器,选择相应的数据库并连接

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E6%96%B0%E5%A2%9E%E6%9C%8D%E5%8A%A1%E5%99%A8.png)



![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E8%BF%9E%E6%8E%A5.png)

然后重启软件



## 连接服务器,选择数据库文档生成器

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E7%94%9F%E6%88%90%E6%96%87%E6%A1%A3.png)



选择数据库和表,点击生成



![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E7%94%9F%E6%88%90.png)



文档就生成好了

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E6%96%87%E6%A1%A3%E7%A4%BA%E8%8C%83.png)



# 方式三. Mysql2docx

## 安装python环境

官网: 

[https://www.python.org/downloads/](https://www.python.org/downloads/)



安装时,勾选加入环境变量

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/python.png)



一定要勾选安装PIP插件

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/pip.png)



## 安装Mysql2docx插件

打开CMD命令窗口,输入

`pip install Mysql2docx`

会自动下载安装Mysql2docx插件

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/Mysql2docx%E5%AE%89%E8%A3%85.png)

安装完提示你升级PIP18,可以不予理会

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/pip18.png)



## 生成文档

CMD命令框继续输入

`python`

进入到了python命令模式

然后分别输入执行以下三条命令

`from Mysql2docx import Mysql2docx`

`m=Mysql2docx()`

`m.do('127.0.0.1','root','password','db_test',3306)`



最终会在C盘用户目录下生成文档

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E7%94%A8%E6%88%B7.png)

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Mysql/Mysql%E5%AF%BC%E5%87%BA%E6%95%B0%E6%8D%AE%E5%BA%93%E8%AE%BE%E8%AE%A1%E6%96%87%E6%A1%A3/%E6%96%87%E6%A1%A33.png)



> 我在连接本地localhost时,生成的文档是空的,不知为何,远程连接数据库是没问题,可能是因为Mysql的版本??

