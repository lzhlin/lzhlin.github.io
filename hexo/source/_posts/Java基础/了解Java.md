---
title: 了解Java
date: 2018-10-16 14:41:45
categories: 
- Java基础篇
- 初识Java
tags: Java
comments: true
---
# Java三大版本
- JavaSE: 标准版 定位在个人计算机应用
- JavaEE: 企业版 定位在服务器端应用
- JavaME: 微型版 定位在消费性电子产品应用

> JavaEE包含JAVASE,所以要先学JavaSE
> JavaME不同于安卓开发,已逐步被安卓取代

<br>

# JDK介绍
Java开发工具包 JDK [下载地址](https://www.oracle.com/technetwork/cn/java/javase/downloads/jdk8-downloads-2133151-zhs.html)
 JRE是Java程序的运行环境
 JVM是实现跨平台的根本
<br>
# Java环境配置
在我的电脑属性中,点击高级系统设置,环境变量,系统变量中,  新建变量,变量名:`JAVA_HOME`,变量值为JDK安装路径
在PATH变量中,加入`%JAVA_HOME%\bin`
JDK1.5以上无需配置classpath
 
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/%E8%AE%BE%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F.png)
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/%E8%AE%BE%E7%BD%AE%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F2.png)
 <br>
 # Java是解释型语言
JDK包括JRE和编译器调试器等用于程序开发的文件
JRE包括JVM虚拟机,库等文件
JVM是执行bytecode字节码的"虚拟计算机"
 
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/JDK-JRE-JVM.png)
 
所以,若只需要运行Java程序则只需安装JRE即可.若需要开发,需下载JDK
 
 `.Java`文件通过编译器生成`.class`文件,最终通过解释器解释运行
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/%E8%BF%90%E8%A1%8C%E8%BF%87%E7%A8%8B.png)

根据不同的操作系统,不同的虚拟机来解释执行
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/Java%E6%89%A7%E8%A1%8C.png)
 
 <br>
 # 简单举例
如 我在F:\mycode下新建文件 `Welcome.java`
{% codeblock Welcome.java lang:Java %}
public class Welcome {
	public static void main(String[] args){
		System.out.println("I'm lpp,Hellow World");
	}
}

class car {

}
{% endcodeblock %}

windows+r打开运行命令框,输入cmd,执行以下命令
`F:` (进入F盘)
`cd F:/mycode` (进入mycode文件夹下)
`javac Welcome.java` (javac命令可以编译java文件,生成class字节码文件)
`java Welcome` (java命令,会解释执行Welcome.class文件)

<br>
>- 一个Java文件可以有多个class类,编译后会生成多个class文件,但是只能有一个public类.
- Java文件名需与其内public类名相同.
- Java执行class文件,需以main方法为入口,否则不可执行.

<br>
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/welcome.png)
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/cmd.png)
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/cmd%E8%BF%90%E8%A1%8C.png)
![](https://javabasics-1257838768.cos.ap-beijing.myqcloud.com/%E5%88%9D%E8%AF%86Java/%E4%BA%86%E8%A7%A3Java/Fpan.png)

 