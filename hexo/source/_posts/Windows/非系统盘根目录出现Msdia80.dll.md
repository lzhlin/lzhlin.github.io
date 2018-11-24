---
title: 非系统盘根目录出现Msdia80.dll
categories: Windows
tags: Windows
comments: true
date: 2018-11-24 20:43:59
---

无意中发现非系统盘根目录下出现Msdia80.dll这样的文件,这是什么呢?

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Windows/%E9%9D%9E%E7%B3%BB%E7%BB%9F%E7%9B%98%E6%A0%B9%E7%9B%AE%E5%BD%95%E5%87%BA%E7%8E%B0Msdia80.dll/msdia80%E6%88%AA%E5%9B%BE.png)



出现此问题的原因：计算机上安装了 Microsoft Visual C++ 2005 可再发行组件时，Msdia80.dll文件被错误安装在其他驱动器的根文件夹中。



它的正确路径应该是"C:\Program Files\Common Files\Microsoft Shared\VC\msdia80.dll" 。

如果在正确路径下有这个文件，那你可以删了这个文件。



如果没有这个文件，解决的方法：

先把这个msdia80.dll复制到C:\Program Files\Common Files\Microsoft Shared\VC\内。



然后管理员运行命令提示符，(用win+R运行CMD时可能会失败)，如图。

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Windows/%E9%9D%9E%E7%B3%BB%E7%BB%9F%E7%9B%98%E6%A0%B9%E7%9B%AE%E5%BD%95%E5%87%BA%E7%8E%B0Msdia80.dll/%E5%91%BD%E4%BB%A4.png)



输入如下命令回车（注意一定不要输错，参考图片）：

`regsvr32 "C:\Program Files\Common Files\Microsoft Shared\VC\msdia80.dll"`



提示成功！这样d/e盘根目录出现的Msdia80.dll文件就可以删除了。

![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/Windows/%E9%9D%9E%E7%B3%BB%E7%BB%9F%E7%9B%98%E6%A0%B9%E7%9B%AE%E5%BD%95%E5%87%BA%E7%8E%B0Msdia80.dll/%E5%B7%B2%E6%88%90%E5%8A%9F.png)



不经过以上步骤随意删除也许会引起未知的奇怪问题，所以遇到dll文件还是要慎重处理



