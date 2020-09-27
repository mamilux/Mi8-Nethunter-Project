# XiaoMi8 Nethunter Project
## Getting Started
Warning: This kernel is intended for hacker technology learning and communication, not for illegal use, all behaviors and responsibilities have nothing to do with me!

The kernel uses Google common kernel to merge CAF production, suitable for MIUI12 and other ROMs

Support all functions on Nethunter official website

Here is the kernel source code:
Here are all the Patch files used: 

## Kernel Function
### Support Nethunter Function
- WIFI Injection IEEE80211 and support 2.4GHZ & 5GHZ
- Support otg MTKMT7601U rt28xx/307x ar9170 rtl8187/8 ZD1201USB.....
- Support rtl88xxau
- HID attack and support DuckyHID
- DriveDroid support
- SYSVIPC (now you can run postgresql normally)
- USB RNDIS
- USB RTL8150/2/3 based ethernet device support
- RFcomm tty support
- USB/UART bluetooth device
- RTL-SDR, AirSpy, Hackrf
- USB serial (now it supports ch340 and pl2303)
- Wireless extension compatible (now you can use iwconfig and set monitor mode)
- Enable Qualcomm WiFi monitor mode, now you can set your network card "wlan0" to monitor mode(No injection support)

### Release kernel Characteristic
- Upstream latest Linux version (4.9.237)
- Merge CAF tag 'LA.UM.8.3.r1-08500-sdm845.0'
- Compiled with Clang 11 + LLD + Polly
- Vibration Control
- KCAL (Colour control)
- Sound Control
- Minimum Brightness Control
- Klapse5.0
- CPU Governors: Schedutil
- Schedutil updated with patches from newer Linux versions
- Using PELT scheduler mechanism
- CPU idle improvements by kerneltoast
- CPU input boost
- NTFS and F2FS file systems supported
- f2fs Rapid GC
- BBR set as default TCP algorithm
- TTL
- Wireguard support
- VDSO for better performance in 32 bit apps
- Unused Drivers And Logging removed for a smaller image
- GPU minimum frequency reduced to 180Mhz
- GPU maximum frequency overclocked to 810Mhz
- Increase Adreno boost, closed by default
- SchedTune and CPUSet
- Dynamic Stune Boost
- Charge_Boost
- boeffla_wakelock_blocker v1.1.0
- Use lz4 as the default ZRAM memory compression algorithm

### How to install or use it
First on the premise of removing the mandatory encryption of data partition, back up your existing boot.img and dtbo.img and flash magisk, then swipe the kernel package into twrp and restart it.
Second enter your system, install kali chroot and reboot.

If you want to use HID,you should run `setprop sys.usb.config win,hid` as root on the terminal.


Please see here to see how to turn wlan0 monitor mode on.


Due to the special nature of the newly added rtl8812au network card, it is not possible to directly use airmon-ng to directly start the monitoring mode, which can be run by the following command:
Xiaomi phone need set wlan2 instead of wlan1
`ip link wlan2 down`
`iw dev wlan2 set type monitor`
`ip link wlan2 up`

### Known Issues
Please tell me

### Thank you list (ranked without distinction)
[Google Common Kernel](https://android.googlesource.com/kernel/common/+/refs/heads/android-4.9-q)
[Twisted Prime](https://github.com/TwistedPrime)
[palaych](https://github.com/palaych)
[osm0sis](https://github.com/osm0sis/AnyKernel3)
[kimocoder](https://github.com/kimocoder)
[johanlike](https://github.com/johanlike)
[simonpunk](https://forum.xda-developers.com/oneplus-5/development/burgerhunter-t3638810)
[h1jacker](https://github.com/h1jacker)
[SDTLB](https://github.com/shandongtlb)