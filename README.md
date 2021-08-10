# Dell Latitude 5175 黑苹果Opencore引导

## 默认建议安装Big Sur
## 配置
### CPU : Intel Core m5-6Y57(1.1GHz/L3 4M)
### Graphics : Intel® HD Graphics 515 
### Sound : Realtek ALC3266 (ALC298)
### Memory : LPDDR3 4GB 1600 MHz(2GB * 2 Dual Channel)
### SSD : TINTEL SSDSCKGF256A5 SATA 256GB 
### Wireless : Intel 8260 AC + 蓝牙4.1
***
## 使用说明
### Opencore版本:0.7.1
### 支持安装Monterey Beta[<sup>1</sup>](#zhuyi)、Big Sur，Catalina、Mojave。
### 声卡注入id：16
### 安装完成Big Sur后进入系统后自己启用AirportItlwm.kext、IntelBluetoothFirmware.kext、IntelBluetoothInjector.kext这三个驱动。以使用自带蓝牙及无线网卡。
### 默认config.plist配置为Big sur版本，如需要安装Catalina请将config_catalina.plist改为config.plist，然后开机之后将IO80211Family_catalina.kext改为IO80211Family.kext并加入config.plist配置内并开机启动。即可使用自带WiFi。
### 当然如果想要安装Mojave也是可以使用config_catalina.plist配置启动，至于WiFi就将IO80211Family_Mojave.kext改为IO80211Family.kext并加入config.plist配置内并开机启动。，然后就OK啦
# Opencore安装Catalina和Big Sur 如下图：
# Big Sur
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Big%20Sur%2011.5.1.png?raw=true)
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Big%20Sur.png?raw=true)
# Catalina
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Catalina.png?raw=true)

<div id="zhuyi"></div>

## 注意
[1] Monterey Beta驱动支持可能有些问题，比如蓝牙驱动有可能出现莫名的问题，加载后甚至不能开机进入系统，所以默认现在是没有加载蓝牙及无线网卡驱动的，无线网卡驱动需要自己去下载相应的Monterey的驱动，系统安装完成后自己尝试
