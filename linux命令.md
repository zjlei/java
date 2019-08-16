# 查看系统信息 #
	
	

 - cpu信息:
 
		lscpu,
		cat /proc/cpuinfo
		pidstat 监控全部或指定进程占用系统资源的情况.
		mpstat 实时系统监控工具 文件/proc/stat
		slabtop 实时显示内核slab缓存信息 /proc/slabinfo

 - member:
 
		free -m
		cat /proc/meminfo
		dmidecode -t memory
		vmstat virtual meomory statistics
 - dmidecode -t bios
	
 - 硬盘分区:
 
		lsblk
		fdisk -l
		df -H
		
 - I/O
	 	
		iozone 文件系统的benchmark
		iotop	用来监视磁盘I/O使用状况top工具
		blktrace 显示block的I/O详细信息的工具.查看CPU,网卡,tty设备
		iostat

 - 查看网络接口:
 
		ifconfig
		ip addr
		ethtool eth0 查看网卡信息
		sar	System Activity Reporter 系统活动情况报告
		tcpdump
		netstat
		nicstat 实时监控网卡及网络流量
		mtr my traceroute 把ping 和traceroute并入一个程序的网络诊断工具
		lsof list open files 列出系统打开文件工具

 - 查看所有卡槽信息:
 
		lspci
		
 - lsscsi
 
		通过运行下面的命令可以列出像硬盘和光驱等 scsi/sata 设备的信息：
	
 - lsusb
 
		lsusb命令能够列出 USB 控制器和与 USB 控制器相连的设备的详细信息。默认情况下，lsusb命令只打印出概要信息。可以通过使用-v参数打印每一个usb端口的详细信息。
		
		
		
 - dmidecode简介

      dmidecode允许你在Linux系统下获取有关硬件方面的信息。dmidecode遵循SMBIOS/DMI标准，其输出的信息包括BIOS、系统、主板、处理器、内存、缓存等等。

      DMI（Desktop Management Interface,DMI）就是帮助收集电脑系统信息的管理系统，DMI信息的收集必须在严格遵照SMBIOS规范的前提下进行。SMBIOS（System Management BIOS）是主板或系统制造者以标准格式显示产品管理信息所需遵循的统一规范。SMBIOS和DMI是由行业指导机构Desktop Management Task Force(DMTF)起草的开放性的技术标准，其中DMI设计适用于任何的平台和操作系统。

			DMI充当了管理工具和系统层之间接口的角色。它建立了标准的可管理系统更加方便了电脑厂商和用户对系统的了解。DMI的主要组成部分是Management Information Format(MIF)数据库。这个数据库包括了所有有关电脑系统和配件的信息。通过DMI，用户可以获取序列号、电脑厂商、串口信息以及其它系统配件信息。
		
-	综合工具

	top

	gprof

	oprofile

	dstat

	strace

	vmstat

	iostat
	
	
	du
	chown
	chmod
	useradd
	userdel
	usermod
	groupadd
	groupdel
	groupmod
	tar