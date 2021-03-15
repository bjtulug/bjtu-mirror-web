---
title: "Gentoo"
description: ""
date: 2021-03-15T18:52:08+08:00
lastmod: 2021-03-15T18:52:08+08:00
draft: false
images: []
menu: ['help']
---

`gentoo` 镜像为 Gentoo Linux 的软件包镜像，包含 distfiles，liveDVD，stage3 等文件，ebuilds 镜像为 `gentoo-portage` 。

## 使用方式

用你喜欢的编辑器编辑 `/etc/portage/make.conf` ，找到 `GENTOO_MIRRORS` 变量，修改为 `GENTOO_MIRRORS="https://mirror.bjtu.edu.cn/gentoo/"` 。

一个完整的 `/etc/portage/make.conf` 文件样例如下（来自一位不愿意透露姓名的热心 Gentoo 用户张三同志）（由于 Gentoo Linux 存在较高配置灵活性，切勿直接复制此文件！）：

```
# These settings were set by the catalyst build script that automatically
# built this stage.
# Please consult /usr/share/portage/config/make.conf.example for a more
# detailed example.
CFLAGS="-march=native -O2 -pipe"
#CXXFLAGS="${CFLAGS} -std=c++14"
CXXFLAGS="${CFLAGS}"
# WARNING: Changing your CHOST is not something that should be done lightly.
# Please consult http://www.gentoo.org/doc/en/change-chost.xml before changing.
CHOST="x86_64-pc-linux-gnu"

# These are the USE flags that were used in addition to what is provided by the
# profile used for building.
nouse="-consolekit -cups -gps -ibus -printsupport -qt4 -qt5 -gtk -gtk2 -gtk3 -wxwidgets -webkit -wayland"

media="alsa ffmpeg flac gstreamer jpeg mp3 mp4 png pulseaudio sound svg theora vpx wavpack webp x264 x265 xvid zvbi"

book="cb chm ebook djvu mobi pdf"

other="256-color acpi avahi bluetooth cjk drm fontconfig geoip git glamor gnutls gpm guile handbook iconv icu ipv6 joystick lapack latex libnotify lzma mtp natspec ncurses networkmanager nls opengl pango postscript samba systemd threads vaapi vala X xft xinerama xorg zeroconf zlib zsh-completion profile"

USE="$nouse $media $book $other"

##grep ^flags /proc/cpuinfo | sed -n 1p | cut -d ":" -f2
CPU_FLAGS_X86="fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx rdtscp lm constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc aperfmperf eagerfpu pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16 xtpr pdcm pcid sse4_1 sse4_2 x2apic popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm ida arat epb pln pts dtherm tpr_shadow vnmi flexpriority ept vpid fsgsbase smep erms xsaveopt sse3 mmxext"

VIDEO_CARDS="intel i965"
ALSA_CARDS="hda-intel"
#INPUT_DEVICES="libinput mouse keyboard joystick"
INPUT_DEVICES="libinput"
MAKEOPTS="--quiet -j3"
EMERGE_DEFAULT_OPS="--keep-going --with-bdeps=y --verbose --quiet"
GENTOO_MIRRORS="https://mirror.bjtu.edu.cn/gentoo/"
PORTAGE_TMPDIR="/tmp"
ACCEPT_KEYWORDS="~amd64"
ACCEPT_LICENSE="*"
PORTAGE_COMPRESS="bzip2"
RUBY_TARGETS="ruby24"
L10N="en en-US zh zh-CN"
LINGUAS="en en_US zh zh_CN"
#DISTDIR="/tmp"
GRUB_PLATFORMS="efi-64"
LLVM_TARGETS=""
```
