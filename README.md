B365ITX-Hackintosh-OC 华擎B365ITX OC配置

主机配置：
------------------------	
CPU：i5 9400F</br>
主板：华擎B365M ITX/AC
显卡：蓝宝石RX570 4G
无线网卡：BCM94360CS2
硬盘：西数SN550nvme固态500G+英睿达120G固态
机箱：SGPC 傻瓜超人k99v2


各硬盘系统分布：
------------------------	
nvme  固态500G：Windows 10 1809 --UEFI引导
英睿达120G固态：macOS 10.15.5 --opencore引导
OC正常引导2个系统

引导工作情况：
------------------------	
此config文件在我设备上正常使用，但不保证你可以直接使用，若因使用此config导致的第三次世界大战、宇宙射线增强、主板
损坏等问题与本人无关！	
注意：必须添加三码才可使用！！！！方法在下面！！！
     无核显（9400F），config未配置核显

正常工作的硬件：
WiFi蓝牙正常  有线网卡正常  独显正常   睡眠正常  唤醒正常  HEVC/H264双硬解正常  FaceTime/短信正常
USB已定制，本人机箱无前面板USB，机型为iMacPro1,1（iMac Pro 2017），修改机型请去掉USBPorts.kext，
改用USBInjectAll.kext，否则可能导致开机键鼠不能使用！

	
机型修改说明：
------------------------	
GenSMBIOS生成的信息对应填入PlatformInfo--Generic下，对应关系如下：

SystemProductName ------ Type
SystemSerialNumber ----- Serial
MLB -------------------- Board Serial
SystemUUID ------------- SmUUID
	
主题说明：config已开启本人修改的官方主题