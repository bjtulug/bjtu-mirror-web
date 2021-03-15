---
title: "Ctan"
description: ""
date: 2021-03-15T18:50:39+08:00
lastmod: 2021-03-15T18:50:39+08:00
draft: false
images: []
menu: ['help']
---

## CTAN (The Comprehensive TeX Archive Network) 镜像源可以使用 TeX Live 管理器 tlmgr 更改。

在命令行中执行

```bash
tlmgr option repository https://mirror.bjtu.edu.cn/ctan/systems/texlive/tlnet
```

即可永久更改镜像源。

如果只需要临时切换，可以用如下命令：

```bash
tlmgr update --all --repository https://mirror.bjtu.edu.cn/ctan/systems/texlive/tlnet
```

其中的 `update --all` 指令可根据需要修改。
