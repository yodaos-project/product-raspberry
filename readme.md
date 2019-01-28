
#树莓派3B+ + seeed 板 实现 rokid 语音音响功能。

##硬件设备：

 树莓派3B+ 开发板 
 ReSpeaker 4-Mic Array for Raspberry Pi Seeed 板
 5V 2000mA mini usb 电源
 耳机、USB 鼠标和键盘 

##软件：

 参考:https://yodaos.rokid.com

##编译方法：

cp ../products/yodaos/rbpi-3b-plus/configs/broadcom_bcm2710_rpi3b_plus_defconfig ../openwrt/.config
cd ../openwrt
make defconfig
make clean;make

##烧写方法

编译后在../openwrt/bin/brcm2708-glibc下 生成openwrt-brcm2708-bcm2710-rpi-3-ext4-factory.img.gz 烧写镜像。
把该镜像烧写到SD卡，把sd插入树莓派中，耳机、seeed 板,鼠标和键盘,插好电源,系统启动。

##配置

   进入https://developer.rokid.com 申请SN 号 和seed 并开通相应技能
上电后在键盘上输入 sn 和 seed 

例如：
   setprop ro.boot.serialno 0501031838000008
   setprop ro.boot.rokidseed 6940ou971E2k0dv72E4oP06h7Fhz89
   setprop ro.devicetypeid 0ABA0AA4F71949C4A3FB0418BF025113 (可选）
   /etc/init.d/vui-daemon restart

现在你可以在手机端下载若琪APP，打开手机蓝牙进行配网,配网成功后就可正常使用。

参考网址：
https://yodaos.rokid.com
https://www.raspberrypi.org
http://wiki.seeedstudio.com/ReSpeaker_4_Mic_Array_for_Raspberry_Pi/


