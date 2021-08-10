---
title: "Gentoo Portage"
description: ""
date: 2021-03-15T18:52:21+08:00
lastmod: 2021-03-15T18:52:21+08:00
draft: false
images: []
menu: ['help']
---

`gentoo-portage` 镜像为 Gentoo Linux 的 ebuilds 镜像，软件包（distfiles, stage3, liveDVD）镜像为 `gentoo` 。

## 使用方式

以下配置方式参见 [Gentoo Handbook: Install Base System: Gentoo ebuild repository](https://wiki.gentoo.org/wiki/Handbook:Parts/Installation/Base#Gentoo_ebuild_repository)，为推荐的配置方法，建议在 `make.conf` 配置的用户按照 Handbook 修改。

1. 首先，创建 `/etc/portage/repos.conf` 目录（如果不存在的话）（我也很纠结他们目录为什么不用 .d 结尾）。

    ```bash
    # mkdir --parents /etc/portage/repos.conf 
    ```

2. 复制一份配置样例到刚才创建的目录。

    ```shell
    # cp /usr/share/portage/config/repos.conf /etc/portage/repos.conf/gentoo.conf 
    ```

3. 最后，修改该文件的 `sync-uri` 变量为 `rsync://mirror.bjtu.edu.cn/gentoo-portage`，样例如下。

    ```conf
    [gentoo]
    location = /usr/portage
    sync-type = rsync
    sync-uri = rsync://mirror.bjtu.edu.cn/gentoo-portage
    auto-sync = yes
   ```

使用 `# emerge --sync` 同步本地的 ebuilds。
