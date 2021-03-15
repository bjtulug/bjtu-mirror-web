---
title: "Pypi"
description: ""
date: 2021-03-15T18:52:56+08:00
lastmod: 2021-03-15T18:52:56+08:00
draft: false
images: []
menu: ['help']
---

## 临时使用

```
pip install -i https://mirror.bjtu.edu.cn/pypi/web/simple/ some-package
```

注意 simple 不能少。

## 设为默认

修改 `~/.config/pip/pip.conf` (Linux), `%APPDATA%\pip\pip.ini` (Windows 10) 或 `$HOME/Library/Application Support/pip/pip.conf` (macOS) (没有就创建一个)， 修改 `index-url` 至镜像，例如

```
[global]
index-url = https://mirror.bjtu.edu.cn/pypi/web/simple/
```

pip 和 pip3 并存时，只需修改 ~/.pip/pip.conf。
