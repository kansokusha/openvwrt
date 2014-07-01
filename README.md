Openvswitch-Openwrt
===================

UPDATE: Works now with OpenWrt trunk and OpenvSwitch v2.1.2

Open vSwitch 2.1.2 (OvS) package for OpenWrt

### Installation in OpenWrt

1. cd $TOPDIR

2. echo 'src-git openvswitch git://github.com/pichuang/openvswitch.git' >> feeds.conf

3. ./scripts/feeds update openvswitch

4. ./scripts/feeds install -a -p openvswitch

5. wget https://gist.githubusercontent.com/pichuang/7372af6d5d3bd1db5a88/raw/4e2290e3e184288de7623c02f63fb57c536e035a/openwrt-add-libatomic.patch -q -O - | patch -p1

6. make menuconfig
 * select Network -> openvswitch-switch, openvswitch-switch, openvswitch-ipsec (Optional)
 * select Advanced configuration options (for developers) -> Toolchain Options -> Binutils Version -> Linaro binutils 2.24

7. echo '# CONFIG_KERNEL_BRIDGE is not set' >> .config

8. make V=s

Development
-----------

Please fork on github and send pull requests.

