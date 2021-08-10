---
title: "Ubuntu"
description: ""
date: 2021-03-15T18:53:17+08:00
lastmod: 2021-03-15T18:53:17+08:00
draft: false
images: []
menu: ['help']
---

Ubuntu 的软件源配置文件是 `/etc/apt/sources.list`。将系统自带的该文件做个备份，将该文件替换为下面内容，即可使用软件源镜像。

1. 20.04 LTS

    ```bash
    # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
    deb https://mirror.bjtu.edu.cn/ubuntu/ focal main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ focal main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ focal-updates main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ focal-backports main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ focal-security main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ focal-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirror.bjtu.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ focal-proposed main restricted universe multiverse
    ```

2. 19.04

    ```bash
    # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
    deb https://mirror.bjtu.edu.cn/ubuntu/ disco main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ disco main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ disco-updates main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ disco-updates main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ disco-backports main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ disco-backports main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ disco-security main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ disco-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirror.bjtu.edu.cn/ubuntu/ disco-proposed main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ disco-proposed main restricted universe multiverse
    ```

3. 19.10

    ```bash
    # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
    deb https://mirror.bjtu.edu.cn/ubuntu/ eoan main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ eoan main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ eoan-updates main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ eoan-updates main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ eoan-backports main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ eoan-backports main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ eoan-security main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ eoan-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirror.bjtu.edu.cn/ubuntu/ eoan-proposed main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ eoan-proposed main restricted universe multiverse
    ```

4. 18.04 LTS

    ```bash
    # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
    deb https://mirror.bjtu.edu.cn/ubuntu/ bionic main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ bionic main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ bionic-updates main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ bionic-backports main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ bionic-security main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ bionic-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirror.bjtu.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ bionic-proposed main restricted universe multiverse
    ```

5. 16.04 LTS

    ```bash
    # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
    deb https://mirror.bjtu.edu.cn/ubuntu/ xenial main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ xenial main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ xenial-updates main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ xenial-security main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ xenial-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirror.bjtu.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ xenial-proposed main restricted universe multiverse
    ```

6. 14.04 LTS

    ```bash
    # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
    deb https://mirror.bjtu.edu.cn/ubuntu/ trusty main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ trusty main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ trusty-updates main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ trusty-updates main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ trusty-backports main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ trusty-backports main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ trusty-security main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ trusty-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirror.bjtu.edu.cn/ubuntu/ trusty-proposed main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ trusty-proposed main restricted universe multiverse
    ```

7. 12.04 LTS

    ```bash
    # 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
    deb https://mirror.bjtu.edu.cn/ubuntu/ precise main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ precise main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ precise-updates main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ precise-updates main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ precise-backports main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ precise-backports main restricted universe multiverse
    deb https://mirror.bjtu.edu.cn/ubuntu/ precise-security main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ precise-security main restricted universe multiverse

    # 预发布软件源，不建议启用
    # deb https://mirror.bjtu.edu.cn/ubuntu/ precise-proposed main restricted universe multiverse
    # deb-src https://mirror.bjtu.edu.cn/ubuntu/ precise-proposed main restricted universe multiverse
    ```
