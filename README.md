B365ITX-Hackintosh-OC 华擎B365ITX OC配置
===
本人主机配置：
------------
	CPU：i5 9400F
	主板：华擎B365M ITX/AC
	显卡：蓝宝石RX570 4G
	WiFi蓝牙：主板自带
	硬盘：西数SN550nvme固态500G+英睿达120G固态+东芝2T机械硬盘
	机箱：SGPC 傻瓜超人k99v2

各硬盘系统分布：<br>
------------
	nvme  固态500G：Windows 10 1809 --UEFI引导
	英睿达120G固态：macOS 10.15.5 --opencore引导
	东芝2T机械硬盘：Windows PE（微PE.ISO） --UEFI引导

config说明：<br>
------------
此config文件在我设备上正常使用，但不保证你可以直接使用，若因使用此config导致的第三次世界大战、宇宙射线增强、主板损坏等问题与本人无关！<br>
<br>
	本config已删除我使用的iMac19.1三码，需要自己生成添加！方法如下：<br>
		01、下载本仓库提供的 GenSMBIOS机型生成器，黑果和win均可运行，黑果下打开GenSMBIOS.command，win下打开GenSMBIOS.bat<br>
		02、打开后按3回车，输入需要的机型。例如iMac19,1，注意字母大小写，逗号为英文状态下输入的<br>
		03、使用ProperTree打开config，将生成的信息对应填入PlatformInfo--Generic下，对应关系如下：<br>
			SystemProductName ------ Type<br>
			SystemSerialNumber ----- Serial<br>
			MLB -------------------- Board Serial<br>
			SystemUUID ------------- SmUUID<br>
<br>
	USB已定制，因机箱无前置USB接口，所以只使用了主板背面的4个USB3.0接口，连接了一个绿联的USB3.0 HUB使用全部正常！需要使用前置USB接口的请自行修改config来关闭USB定制，推荐使用ProperTree来修改，方法如下：<br>
	01、将Kernel--Add--7目录的USBInjectAll.kext  |  Enabled属性改为 Ture  #开启USB驱动
	02、将Kernel--Add--8目录的USBPorts.kext  |  Enabled属性改为 False  #关闭USB定制驱动
	03、将Kernel--Add--8目录的USBPower.kext  |  Enabled属性改为 False  #关闭USB定制驱动依赖
	04、将Kernel--Quirks--XhciPortLimit改为 Ture  #开启USB端口限制，Mac主板限制USB端口数量，所以需要打开限制
注：开机后可自行定制USB，替换自己定制的USBPorts.kext，将上述4处修改为为相反属性即可。
<br>
本人CPU为9400F，无核显，所以没有配置核显，会导致核显无法使用，需要使用核显的需自行解决。<br>
WIFI未驱动，蓝牙正常，有线网卡正常，独显正常、睡眠正常<br>
	