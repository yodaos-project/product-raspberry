# YODAOS Raspberry

YODAOS product for the raspberry 3b+ with Seeed audio board.

### Hardware

- Raspberry 3b+ Devboard
- ReSpeaker 4-Mic Array for Raspberry Pi Seeed board
- 5V 2000mA mini USB power

### Build

```bash
$ cd ./openwrt
$ cp ../products/yodaos/rbpi-3b-plus/configs/broadcom_bcm2710_rpi3b_plus_defconfig .config
$ make defconfig && make
```

### Flush image

1. follow the above steps.
2. find `openwrt-brcm2708-bcm2710-rpi-3-ext4-factory.img.gz` under `openwrt/bin/brcm2708-glibc`.
3. flush the above `.img` file to SD Card and insert to raspberry.
4. reboot the system.

### Speech Registeration

To use the Rokid's speech service, developers need to register an account at [https://developer.rokid.com](https://developer.rokid.com),
and register SN and seed number and configure your skills by following steps:

```bash
$ setprop ro.boot.serialno <SN>
$ setprop ro.boot.rokidseed <Device seed>
$ /etc/init.d/vui-daemon restart
```

### References

- YODAOS Website: https://yodaos.rokid.com
- Raspberry: https://www.raspberrypi.org
- Seeed Studio: http://wiki.seeedstudio.com/ReSpeaker_4_Mic_Array_for_Raspberry_Pi/

### License

Apache 2.0
