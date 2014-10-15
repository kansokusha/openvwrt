OpenvWrt
===================

Open vSwitch 2.3.0 (OvS) package for OpenWrt "CHAOS CALMER" (trunk, r42165)

From NOW, OpenvSwitch had been add to [OpenWrt Packages Repository](https://github.com/openwrt/packages/tree/master/net/openvswitch), so support has ended.


## Installation in OpenWrt

1. cd $TOPDIR

2. echo 'src-git openvswitch git://github.com/pichuang/openvwrt.git' >> feeds.conf

3. ./scripts/feeds update openvswitch

4. ./scripts/feeds install -a -p openvswitch

5. wget https://gist.githubusercontent.com/pichuang/7372af6d5d3bd1db5a88/raw/4e2290e3e184288de7623c02f63fb57c536e035a/openwrt-add-libatomic.patch -q -O - | patch -p1

6. make menuconfig
 * select Network -> openvswitch-switch, openvswitch-switch, openvswitch-ipsec (Optional)
 * select Advanced configuration options (for developers) -> Toolchain Options -> Binutils Version -> Linaro binutils 2.24
 * UNSELECT Advanced configuration options (for developers) -> Target Options -> Build packages with MIPS16 instructions

7. echo '#CONFIG_KERNEL_BRIDGE is not set' >> .config

8. make V=s

**!WARNING!** You need repeat step 7 and 8 after you enter "make menuconfig".


## Enviroment
* Hardware: D-LINK Dir-835
* Build enviroment
 * gcc version 4.9.0 20140604 (prerelease) (GCC)
 * Ubuntu 14.04.1 x86_64

Q&A
---

1. How to build OpenWrt?
 * Please read [Roan's blog Compiled OpenWrt](http://roan.logdown.com/posts/165911-compiled-openwrt) 

2. How to set OpenvSwitch configuration?
 * Please read [Roan's blog Set OpenvSwitch](http://roan.logdown.com/posts/191801-set-openvswitch)

3. No works?
 * Try reboot and ```telnet 192.168.1.1```
 * or, ```make clean``` rebuild it.

Screenshot
----------

![alt tag](https://lh6.googleusercontent.com/-Ix65c7GZIWc/U-2oTcwL4VI/AAAAAAAAFKs/HVAIJYkWdFY/w622-h425-no/Capture.PNG)

Development
-----------

Please fork on github and send pull requests.

