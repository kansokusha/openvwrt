openvswitch
===========

UPDATE: Works now with OpenWrt "Barrier Breaker" (Bleeding Edge)

Open vSwitch 2.1.0 (OvS) package for OpenWrt

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
> make menuconfig
>
> select Network -> openvswitch-switch, openvswitch-brcompat, openvswitch-switch, openvswitch-ipsec (Optional)
> select Advanced configuration options (for developers) -> Toolchain Options -> Binutils Version -> Linaro binutils 2.24
>
> echo '# CONFIG_KERNEL_BRIDGE is not set' >> .config




Development
-----------

Please fork on github and send pull requests.
