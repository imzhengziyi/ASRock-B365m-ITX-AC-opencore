介绍
===
>>本人机器配置
------------
>>>CPU：i5 9400F<br>
>>>主板：华擎B365M ITX/AC<br>
>>>显卡：蓝宝石RX570 4G<br>
>>>WiFi蓝牙：主板自带<br>
>>>硬盘：西数SN550nvme固态500G+英睿达120G固态+东芝2T机械硬盘<br>
>>>机箱：SGPC 傻瓜超人k99v2

>>各硬盘系统分布：<br>
------------
>>>nvme  固态500G：Windows 10 1809 --UEFI引导<br>
>>>英睿达120G固态：macOS 10.15.5 --opencore引导<br>
>>>东芝2T机械硬盘：Windows PE（微PE.ISO） --UEFI引导<br>

>>config说明：<br>
------------
>>>	此config文件在我设备上正常使用，但不保证你可以直接使用，若因使用此config导致的第三次世界大战、宇宙射线增强、主板损坏等问题与本人无关！<br>
<br>
>>>USB已定制，因机箱无前置USB接口，所以只使用了主板背面的4个USB3.0接口，连接了一个绿联的USB3.0 HUB使用全部正常！需要使用前置USB接口的请自行修改config，推荐使用ProperTree来修改，方法如下：<br>
>>>>01、将Kernel--Add--7目录的USBInjectAll.kext  |  Enabled属性改为 Ture  #开启USB驱动<br>
>>>>02、将Kernel--Add--8目录的USBPorts.kext  |  Enabled属性改为 False  #关闭USB定制驱动<br>
>>>>03、将Kernel--Add--8目录的USBPower.kext  |  Enabled属性改为 False  #关闭USB定制驱动依赖<br>
>>>>04、将Kernel--Quirks--XhciPortLimit改为 Ture  #开启USB端口限制，Mac主板限制USB端口数量，所以需要打开限制<br>