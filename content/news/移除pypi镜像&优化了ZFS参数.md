---
title: "移除pypi镜像&优化了ZFS参数"
description: ""
date: 2020-02-23T00:00:00+08:00
lastmod: 2020-02-23T00:00:00+08:00
draft: false
author: "Chestnut"
---

因pypi占用了接近三分之一的磁盘空间，且实际访问量过小，同步压力较大，为保证整体服务质量，将pypi镜像进行了移除，原有地址将被301重定向至tuna源。

优化了ZFS的参数，极大降低了磁盘的读写压力，提高了镜像站的吞吐量。
