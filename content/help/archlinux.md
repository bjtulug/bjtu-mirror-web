---
title: "Archlinux"
description: ""
date: 2021-03-15T18:46:31+08:00
lastmod: 2021-03-15T18:46:31+08:00
draft: false
images: []
menu: ['help']
---

编辑 `/etc/pacman.d/mirrorlist`， 在文件的最顶端添加：`Server = https://mirror.bjtu.edu.cn/archlinux/$repo/os/$arch`

更新软件包缓存：`# pacman -Syy`