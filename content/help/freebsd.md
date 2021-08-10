---
title: "Freebsd"
description: ""
date: 2021-03-15T18:51:08+08:00
lastmod: 2021-03-15T18:51:08+08:00
draft: false
images: []
menu: ['help']
---

## pkg 源:pkg源提供二进制安装包.

FreeBSD中pkg源分为系统级和用户级两个源.不建议直接修改/etc/pkg/FreeBSD.conf,因为该文件会随着基本系统的更新而发生改变.

创建用户级源目录:

`#mkdir -p /usr/local/etc/pkg/repos`

创建用户级源文件:

`#ee /usr/local/etc/pkg/repos/bjtu.conf`

写入以下内容:

```conf
bjtu: {
  url: "pkg+http://freebsd-pkg.mirror.bjtulug.org/${ABI}/quarterly",
  mirror_type: "srv",
  signature_type: "none",
  fingerprints: "/usr/share/keys/pkg",
  enabled: yes
}
 FreeBSD: { enabled: no }
```

若要获取滚动更新的包,请将 `quarterly` 修改为 `latest` .请注意, `CURRENT` 版本只有 `latest` .

若要使用https,请先安装security/ca_root_nss,并将 `http` 修改为 `https` ,最后使用命令 `#pkg update -f` 刷新缓存即可.

## ports源:提供源码方式安装软件的包管理器

创建或修改文件`#ee /etc/make.conf`:

写入以下内容:

`MASTER_SITE_OVERRIDE?=http://freebsd-pkg.mirror.bjtulug.org/ports-distfiles/`

## portsnap源:打包的ports文件

编辑portsnap配置文件 `#ee /etc/portsnap.conf` :

将 `SERVERNAME=portsnap.FreeBSD.org` 修改为 `SERVERNAME=freebsd-portsnap.mirror.bjtulug.org`

获取portsnap更新:

`#portsnap fetch extract`

## freebsd-update源:提供基本系统更新

编辑 `#ee /etc/freebsd-update.conf` 文件:

将 `ServerName update.FreeBSD.org` 修改为 `ServerName freebsd-update.mirror.bjtulug.org`

例:从FreeBSD 11升级到12.0

`#freebsd-update -r 12.0-RELEASE upgrade`
