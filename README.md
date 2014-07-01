openvswitch
===========

UPDATE: Works now with OpenWrt trunk and OpenvSwitch v2.1.2

Open vSwitch 2.1.2 (OvS) package for OpenWrt

Installation
------------

Install this as a feed!

### Installation in OpenWrt

> cd $TOPDIR
> 
> echo 'src-git openvswitch git://github.com/pichuang/openvswitch.git' >> feeds.conf
>
> ./scripts/feeds update openvswitch
>
> ./scripts/feeds install -a -p openvswitch
>
> wget https://gist.githubusercontent.com/pichuang/7372af6d5d3bd1db5a88/raw/4e2290e3e184288de7623c02f63fb57c536e035a/openwrt-add-libatomic.patch -q -O - | patch -p1
>
> make menuconfig
>
> select Network -> openvswitch-switch, openvswitch-brcompat, openvswitch-switch, openvswitch-ipsec (Optional)
>
> select Advanced configuration options (for developers) -> Toolchain Options -> Binutils Version -> Linaro binutils 2.24
>
> echo '# CONFIG_KERNEL_BRIDGE is not set' >> .config




Development
-----------

Please fork on github and send pull requests.
