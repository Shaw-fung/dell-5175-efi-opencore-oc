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
- #### 目前建议安装Big Sur
- #### Opencore版本:0.7.1[<sup>(1)</sup>](#zhuyi)
- #### 系统无线网卡及蓝牙驱动由OpenIntelWireless[<sup>(2)</sup>](#zhuyi)提供
- #### 支持安装Monterey Beta[<sup>(3)</sup>](#zhuyi)、Big Sur，Catalina、Mojave。
### BIOS 设置
- #### Boot Sequence 设置UEFI启动
- #### Secure Boot Enable 设置为Disabled
- #### Intel® SGX[<sup>TM</sup>] Enable 设置为Disabled
- #### 关闭VT For Direct I/O
- #### 关闭Virtualization
- #### 如设置有问题，可以自行多使用搜索引擎（Google，Baidu，etc.），看看设置内容，可参考别的机型(一般来说黑苹果BIOS所需要的设置的项目都差不多，没有的就不用管)。
### macOS Big Sur 使用说明
- #### 安装完成Big Sur后进入系统后自己启用AirportItlwm.kext、IntelBluetoothFirmware.kext、IntelBluetoothInjector.kext这三个驱动。以使用自带蓝牙及无线网卡。
### macOS Catalina 使用说明
- #### 默认config.plist配置为Big sur版本，如需要安装Catalina请将config_catalina.plist改为config.plist，然后开机之后将IO80211Family_catalina.kext改为IO80211Family.kext并加入config.plist配置内并开机启动。即可使用自带无线网卡。蓝牙驱动请使用IntelBluetoothFirmware.kext、IntelBluetoothInjector.kext。
### macOS Mojave 使用说明
- #### 默认config.plist配置为Big sur版本，如需要安装Mojave也是可以使用config_catalina.plist配置启动，请将config_catalina.plist改为config.plist，至于自带无线网卡就把O80211Family_Mojave.kext改为IO80211Family.kext并加入config.plist配置内并开机启动。蓝牙驱动请使用IntelBluetoothFirmware.kext、IntelBluetoothInjector.kext。
### macOS Monterey 使用说明
- #### Monterey由于蓝牙框架改动，需要使用新的蓝牙驱动，需要将原IntelBluetoothInjector.kext开机加载取消，改用BlueToolFixup.kext[<sup>(4)</sup>](#zhuyi)开机加载。IntelBluetoothFirmware.kext这个不需要变动，仍然保持开机加载。
- #### Monterey安装的时候如需要启动自带WiFi，则需要将AirportItlwm.kext这个文件开机加载取消，改用开机加载AirportItlwm_Monterey.kext这个驱动，然后就可以正常使用自带WiFi驱动。
***
## Opencore安装Big Sur和Catalina成功截图如下：
### Big Sur：
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Big%20Sur.png?raw=true)
***
### Catalina：
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Catalina.png?raw=true)

***
<div id="zhuyi"></div>

### 注意
[1] Opencore Github地址：[https://github.com/acidanthera/OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)  
[2] OpenIntelWireless Github地址：[https://github.com/OpenIntelWireless](https://github.com/OpenIntelWireless)  
[3] Monterey Beta，由于暂时是Beta版本驱动支持可能有些问题，比如蓝牙驱动有可能出现莫名的问题，加载后甚至不能开机进入系统，所以默认是没有加载蓝牙及无线网卡驱动的，无线网卡驱动需要自己选择加载驱动。  
[4] BlueToolFixup.kext Github地址：[https://github.com/acidanthera/BrcmPatchRAM](https://github.com/acidanthera/BrcmPatchRAM)  
