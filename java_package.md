# java包 #


- 以最终用户角度:

	JAR,war,ear包就是一种封装,他们不需要知道压缩包中有多少个.class文件，每个文件中的功能与作用.运行可以得到他们希望的结果。

- JAR包文件结构:

	1. jar格式以流行的 ZIP 文件格式为基础.与 ZIP 文件不同的是，JAR 文件不仅用于压缩和发布，而且还用于部署和封装库、组件和插件程序，并可被像编译器和 JVM 这样的工具直接使用.
	
	2. JAR 文件与 ZIP 文件唯一的区别就是在 JAR 文件的内容中，包含了一个 META-INF/MANIFEST.MF 文件，这个文件是在生成 JAR 文件的时候自动创建的。

	3.	tools.jar

  		|  resource.xml// 资源配置文件

 		|  other.xml

		|— META-INF   

 		|MANIFEST.MF // jar包的描述文件

		|— com   // 类的包目录

		|—test  

			util.class // java类文件

- war包文件结构:

	1. WAR(Web Archive file)网络应用程序文件，是与平台无关的文件格式，它允许将许多文件组合成一个压缩文件。war专用在web方面 。
	JAVA WEB工程，都是打成WAR包进行发布。

	2. webapp.war

		  |    index.jsp
		
		  |— images
		
		  |— META-INF
		
		  |— WEB-INF
	
		          |   web.xml                   // WAR包的描述文件
	
		          |— classes
		
		          |		action.class       // java类文件
		
		          |— lib
		                other.jar             // 依赖的jar包
		                share.jar


