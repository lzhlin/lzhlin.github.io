---
title: MybatisPlugin和ledis插件破解
categories: IntelliJ IDEA
tags: IntelliJ IDEA
comments: true
date: 2018-11-25 20:33:29
---

MybatisPlugin插件和ledis(IDEA Redis可视化工具)默认是收费的

<!-- more -->

之前找到的这个破解方式,作者地址已经被封了,还好还留有破解的包,放硬盘里了

### ideaagent v1.2 (破解jar)

Mybatis plugin v3.58 crack (mybatis正版插件)
Iedis v2.56 crack (redis正版插件)
支持 IntelliJ IDEA 2018.1

下载地址: 

ideaagent 链接：[https://pan.baidu.com/s/1hb7CHytSWsvuOaSBYmwfdw ](https://pan.baidu.com/s/1hb7CHytSWsvuOaSBYmwfdw )
提取码：bh5g 

Mybatis plugin v3.58链接：https://pan.baidu.com/s/1Ffzpe94FDvGJbkMJVc9rrw 
提取码：2pkb 

Iedis v2.56链接：https://pan.baidu.com/s/1gsFJ4aNrBa-08tZlmLucRg 
提取码：nqm3 

IntelliJ IDEA 2018.1.3链接：https://pan.baidu.com/s/1evQ12p0dwmBUgukEFdyGUA 
提取码：b0y2 

> 我之前有试过其他版本的插件或者其他版本的idea 破解不能成功,所以只能用对应版本的



### 破解方法

1. 先安装插件

   进入到setting设置面板,进入plugins,点击安装本地插件Install plugin fromdisk...

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/IntelliJ%20IDEA/MybatisPlugin%E5%92%8Cledis%E6%8F%92%E4%BB%B6%E7%A0%B4%E8%A7%A3/%E6%8F%92%E4%BB%B6%E5%AE%89%E8%A3%85.png)

分别选择安装`Mybatis plugin v3.58`和`Iedis v2.56 crack`

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/IntelliJ%20IDEA/MybatisPlugin%E5%92%8Cledis%E6%8F%92%E4%BB%B6%E7%A0%B4%E8%A7%A3/%E9%80%89%E6%8B%A9%E6%8F%92%E4%BB%B6%E5%AE%89%E8%A3%85.png)



![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/IntelliJ%20IDEA/MybatisPlugin%E5%92%8Cledis%E6%8F%92%E4%BB%B6%E7%A0%B4%E8%A7%A3/%E5%B7%B2%E5%8A%A0%E5%85%A5.png)



可以看到 两个插件已经加入了插件列表  此时重启idea

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/IntelliJ%20IDEA/MybatisPlugin%E5%92%8Cledis%E6%8F%92%E4%BB%B6%E7%A0%B4%E8%A7%A3/%E7%AD%89%E5%BE%85.png)

重启后在此页面可能会卡,我等了很久,最后任务管理器强制关闭了

再次打开以后,可以看到插件是需要付费才给权限



### 破解



打开 idea.vmoptions (Help -> Edit Custom VM Options…)

最下方插入 `-javaagent:E:\ideaagent-1.2.jar`

>  -javaagent: +  破解文件的路径,此路径不可以有中文

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/IntelliJ%20IDEA/MybatisPlugin%E5%92%8Cledis%E6%8F%92%E4%BB%B6%E7%A0%B4%E8%A7%A3/vmoption.png)



然后重启软件

会提示一个认证信息,点击accept

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/IntelliJ%20IDEA/MybatisPlugin%E5%92%8Cledis%E6%8F%92%E4%BB%B6%E7%A0%B4%E8%A7%A3/accept.png)



>  如果idea版本不对,有可能完全打不开程序,点击没反应
>
>  去用户目录下,修改idea.exe.vmoptions文件,删除加的那句话即可
>
>  破解完成后,破解文件即可删除

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/IntelliJ%20IDEA/MybatisPlugin%E5%92%8Cledis%E6%8F%92%E4%BB%B6%E7%A0%B4%E8%A7%A3/%E7%94%A8%E6%88%B7.png)