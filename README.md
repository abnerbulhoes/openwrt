# My OpenWRT files and configs
I had a hard time making my OpenWRT router work with some of my 3G dongles, this repository contains some files and configs to make 3G dongle work with my OpenWRT router.
Might be useful to someone else.

Router Details
--------------
* Router: TP-Link TL-WDR4300 v1
* OpenWRT Firmware: OpenWrt Barrier Breaker 14.07 / LuCI Trunk (0.12+svn-r10530)


Working USB 3G Dongles
----------------------
* Huawey E1746 (recognized as: "Huawei Technologies Co., Ltd. E169/E620/E800 HSDPA Modem")


Files
-----

* *3g.chat -> /etc/chatscripts/3g.chat*  -  Replacement chat script for 3G connectivity. Default script requires tunning, this works with a lot of modems (pulled from an Ubuntu 14.04).
* *proto_3g.lua -> /usr/lib/lua/luci/model/cbi/admin_network/proto_3g.lua - Luci network config script for 3G interface. For some reason package that contained this file is not found online anymore.

Installation
------------
First follow the OpenWRT instructions http://wiki.openwrt.org/doc/recipes/3gdongle.
Then, if needed, copy the files of this repo on the corresponding paths, be smart and do backups prior copying.
Notice that proto_3g.lua is only needed if you want to use the Luci GUI to setup the interface for your dongle (must have Luci installed).
