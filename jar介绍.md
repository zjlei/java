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

2019/7/27 15:29:22 