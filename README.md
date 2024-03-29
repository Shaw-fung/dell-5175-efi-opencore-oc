## Dell Latitude 5175 黑苹果 Opencore[<sup>(1)</sup>](#zhuyi)引导

### 配置
- #### CPU : Intel Core m5-6Y57(1.1GHz/L3 4M)
- #### Graphics : Intel® HD Graphics 515 
- #### Sound : Realtek ALC3266 (ALC298)
- #### Memory : LPDDR3 4GB 1600 MHz(2GB * 2 Dual Channel)
- #### SSD : INTEL SSDSCKGF256A5 SATA 256GB 
- #### Wireless : Intel 8260 AC + 蓝牙4.1
- #### Dell Latitude 5175 原装键盘底座
***
### 安装说明
- #### 目前建议安装Monterey；
- #### Opencore版本:0.7.5[<sup>(1)</sup>](#zhuyi)；
- #### 系统无线网卡及蓝牙驱动由OpenIntelWireless[<sup>(2)</sup>](#zhuyi)提供；
- #### 支持安装Monterey[<sup>(3)</sup>](#zhuyi)、Big Sur，Catalina、Mojave。
### BIOS 设置
- #### Boot Sequence 设置UEFI启动
- #### Secure Boot Enable 设置为Disabled
- #### Intel® SGX<sup>TM</sup> Enable 设置为Disabled
- #### 关闭VT For Direct I/O
- #### 关闭Virtualization
- #### 如设置有问题，可以自行多使用搜索引擎（Google，Baidu，etc.），看看设置内容，可参考别的机型(一般来说黑苹果BIOS所需要的设置的项目都差不多，没有的就不用管)。
### macOS Big Sur 及macOS Monterey 使用说明
- #### Big Sur安装完成后修改序列号即可使用。
- #### Monterey由于蓝牙框架改动，使用BlueToolFixup.kext[<sup>(4)</sup>](#zhuyi)驱动，目前蓝牙问题已经修复。
### macOS Catalina 使用说明
- #### Catalina安装完成后修改序列号即可使用。
### macOS Mojave 使用说明
- #### 如需要安装Mojave，请将AirportItlwm_Mojave.kext加入config.plist配置内并开机启动，方可使用自带WiFi。
***
如果有问题，欢迎提交提问讨论，[我要提交问题](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/issues/new)！
***
## Opencore安装Monterey、Big Sur和Catalina成功截图如下：
### Monterey：
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Monterey.png?raw=true)
***
### Big Sur：
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Big%20Sur.png?raw=true)
***
### Catalina：
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Catalina.png?raw=true)
****
## 更新日志
#### 2021-11-12
- 支持Big sur及monterey安装；
- Intel WiFi及蓝牙可以使用，已经修复Monterey下蓝牙问题。
***
<div id="zhuyi"></div>

### 注意
[1] Opencore Github地址：[https://github.com/acidanthera/OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)  
[2] OpenIntelWireless Github地址：[https://github.com/OpenIntelWireless](https://github.com/OpenIntelWireless)  
[3] Monterey，原蓝牙驱动支持有些问题，现在已经修复。  
[4] BlueToolFixup.kext Github地址：[https://github.com/acidanthera/BrcmPatchRAM](https://github.com/acidanthera/BrcmPatchRAM)  
