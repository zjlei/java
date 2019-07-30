# jar介绍 #


1. 主操作模式


	-c == --create 创建文档

	-u == --update 更新现有jar档案

	-t == --list 列出档案目录

	-x == --extract 从档案中提取指定的文件

	-d == --describe-module 输出模块描述符或自动模块名称

	-i == --generate-index=FILE 指定的jar档案生成


2. 任意模式下有效的操作修饰符:


	-C DRI	调到指定目录

	-f == --file=FILE 档案文件名.省略时,基于操作使用stdin或stdout

	-v == --verbose 在标准输出中生成详细输出


3. 在创建和更新模式下有效的操作修饰符


	-e == --main-class=CLASSNAME 	可执行jar程序入口

	-m == --mainfest=FILE 	包含指定清单文件中的清单信息

	-M == --no-mainfest 				不为条目创建清单文件
	  --module-version=VERSION	创建模块化or更新jar时, 模块版本
	  --hash-modules=PATTERN

	-p == --module-path		模块被依赖对象的位置,用于生成散列


4. 只在创建or更新和生成索引模式下有效


	-0 == --no-compress 仅存储;不使用zip压缩

5.	网络生成jar

	1. 成jar包的URL `URL u=new URL("jar:"+"FirstAppplet.jar"+!/");`
	
	2. 建立jarURLConnection对象 `JarURLConnection juc=(JarURLConnection)u.openConnection();`
	
	3. 返回jar包中主类的名字:     Attributes attr=juc.getMainAttributes();
String name=attr.getValue("Mani-Class");

	4. 根据得到的主类名创建Class对象: `Class c=Class.forName(name);`


**Java调用类的顺序：java\lib\ext中的类--->Manifest.mf中指定的类-->当前目录中的类-->set CLASSPATH中指定的类。**

2019/7/27 15:29:22 