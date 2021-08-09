# Dell Latitude 5175 黑苹果Opencore引导
## 配置
### CPU : Intel Core m5-6Y57(1.1GHz/L3 4M)
### Graphics : Intel® HD Graphics 515 
### Sound : Realtek ALC3266 (ALC298)
### Memory : LPDDR3 4GB 1600 MHz(2GB * 2 Dual Channel)
### SSD : TINTEL SSDSCKGF256A5 SATA 256GB 
### Wireless : Intel 8260 AC + 蓝牙4.1
***
## 说明
### 声卡注入id：16
### 默认config.plist配置为Big sur版本，如需要安装Catalina请将config_catalina.plist改为config.plist，然后开机之后将IO80211Family_catalina.kext改为IO80211Family.kext并加入config.plist配置内并开机启动。即可使用自带WiFi。
### 当然如果想要安装Mojave也是可以使用config_catalina.plist配置启动，至于WiFi就自己去下载AirportItlwm_Mojave.kext然后提取Mojave里面的IO80211Family.kext并将AirportItlwm.kext放入Contents/PlugIns/里面，添加入配置，然后就OK啦
# Opencore安装Catalina和Big Sur 如下图：
# Big Sur
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Big%20Sur%2011.5.1.png?raw=true)
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Big%20Sur.png?raw=true)
# Catalina
![avatar](https://github.com/Shaw-fung/dell-5175-efi-opencore-oc/blob/main/Catalina.png?raw=true)
