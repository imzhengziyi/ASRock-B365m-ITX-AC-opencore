B365ITX-Hackintosh-OC 华擎B365ITX OC配置
===
主机配置：
------------
	CPU：i5 9400F
	主板：华擎B365M ITX/AC
	显卡：蓝宝石RX570 4G
	无线网卡：BCM94360CS2
	硬盘：西数SN550nvme固态500G+英睿达120G固态+东芝2T机械硬盘
	机箱：SGPC 傻瓜超人k99v2

各硬盘系统分布：<br>
------------
	nvme  固态500G：Windows 10 1809 --UEFI引导
	英睿达120G固态：macOS 10.15.5 --opencore引导
	东芝2T机械硬盘：Windows PE（微PE.ISO） --UEFI引导
	OC正常引导3个系统，显示3个菜单Windows（PE）、Windows、MacOS

引导工作情况：<br>
------------
	此config文件在我设备上正常使用，但不保证你可以直接使用，若因使用此config导致的第三次世界大战、宇宙射线增强、主板损坏
	等问题与本人无关！
	
	WiFi蓝牙正常
	有线网卡正常
	独显正常
	睡眠正常
	唤醒正常
	原生电源管理正常
	HEVC/H264双硬解正常
	FaceTime/短信正常
	
	无核显（9400F），config未配置核显
	
	建议使用GenSMBIOS重新计算三码
	config编辑工具和GenSMBIOS工具需要python环境，请先安装！
	打包下载（含python）：https://github.com/imzhengziyi/Hackintosh-tools
	GenSMBIOS官方库：https://github.com/corpnewt/GenSMBIOS
	ProperTree官方库：https://github.com/corpnewt/ProperTree
	
三码替换说明：<br>
------------
	
	01、下载本仓库提供的 GenSMBIOS机型生成器，黑果和win均可运行，黑果下打开GenSMBIOS.command，win下打开
	GenSMBIOS.bat
	02、打开后按3回车，输入需要的机型。例如iMac19,1，注意字母大小写，逗号为英文状态下输入的
	03、使用ProperTree打开config，将生成的信息对应填入PlatformInfo--Generic下，对应关系如下：
		SystemProductName ------ Type
		SystemSerialNumber ----- Serial
		MLB -------------------- Board Serial
		SystemUUID ------------- SmUUID
	
主题说明：<br>
------------
	config已开启本人修改的官方主题，请往远景论坛查看
	链接：http://bbs.pcbeta.com/viewthread-1860685-1-1.html
