 
CATALINA_OPTS="-Xdebug -Xrunjdwp:transport=dt_socket,address=60222,suspend=n,server=y"
JAVA支持调试功能，并提供了一个简单的调试工具JDB，其可支持设置断点及线程级的调试；

2. 各参数解释：

-Xdebug是通知JVM工作在DEBUG模式下

-Xrunjdwp是通知JVM使用(java debug wire protocol)来运行调试环境。该参数同时了一系列的调试选项：

transport指定了调试数据的传送方式，dt_socket是指用SOCKET模式，另有dt_shmem指用共享内存方式，其中，dt_shmem只适用于Windows平台。
server参数是指是否支持在server模式的VM中.
onthrow指明，当产生该类型的Exception时，JVM就会中断下来，进行调式。该参数可选。
launch指明，当JVM被中断下来时，执行的可执行程序。该参数可选
suspend指明，是否在调试客户端建立起来后，再执行JVM。
onuncaught(=y或n)指明出现uncaught exception 后，是否中断JVM的执行.