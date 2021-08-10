---
title: "Repoforge"
description: ""
date: 2021-03-15T18:53:02+08:00
lastmod: 2021-03-15T18:53:02+08:00
draft: false
images: []
menu: ['help']
---

## 添加 Repoforge 仓库

1. 运行 `cat /etc/redhat-release` 获取 EL 版本号（如 EL6, EL7 等）
2. 向系统中添加 Repoforge 的 GPG 公钥：`rpm --import https://mirror.bjtu.edu.cn/repoforge/RPM-GPG-KEY.dag.txt`
3. 运行下列命令：

   1. EL版本7

       ```bash
       sudo cat > /etc/yum.repos.d/rpmforge.repo << EOF
       [rpmforge]
       name = RHEL $releasever - RPMforge.net - dag
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/rpmforge
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge
       enabled = 1
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-extras]
       name = RHEL $releasever - RPMforge.net - extras
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/extras
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-extras
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-testing]
       name = RHEL $releasever - RPMforge.net - testing
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/testing
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-testing
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1
       EOF
       ```

   2. EL版本6

       ```bash
       sudo cat > /etc/yum.repos.d/rpmforge.repo << EOF
       [rpmforge]
       name = RHEL $releasever - RPMforge.net - dag
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/rpmforge
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge
       enabled = 1
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-extras]
       name = RHEL $releasever - RPMforge.net - extras
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/extras
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-extras
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-testing]
       name = RHEL $releasever - RPMforge.net - testing
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/testing
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-testing
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1
       EOF
       ```

   3. EL版本5

       ```bash
       sudo cat > /etc/yum.repos.d/rpmforge.repo << EOF
       [rpmforge]
       name = RHEL $releasever - RPMforge.net - dag
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/rpmforge
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge
       enabled = 1
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-extras]
       name = RHEL $releasever - RPMforge.net - extras
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/extras
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-extras
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-testing]
       name = RHEL $releasever - RPMforge.net - testing
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/testing
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-testing
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1
       EOF
      ```

   4. EL版本4

       ```bash
       sudo cat > /etc/yum.repos.d/rpmforge.repo << EOF
       [rpmforge]
       name = RHEL $releasever - RPMforge.net - dag
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/rpmforge
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge
       enabled = 1
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-extras]
       name = RHEL $releasever - RPMforge.net - extras
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/extras
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-extras
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-testing]
       name = RHEL $releasever - RPMforge.net - testing
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/testing
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-testing
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1
       EOF
       ```

   5. EL版本3

       ```bash
       sudo cat > /etc/yum.repos.d/rpmforge.repo << EOF
       [rpmforge]
       name = RHEL $releasever - RPMforge.net - dag
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/rpmforge
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge
       enabled = 1
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-extras]
       name = RHEL $releasever - RPMforge.net - extras
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/extras
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-extras
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1

       [rpmforge-testing]
       name = RHEL $releasever - RPMforge.net - testing
       baseurl = https://mirror.bjtu.edu.cn/repoforge/redhat/el7/en/$basearch/testing
       mirrorlist = http://mirrorlist.repoforge.org/el7/mirrors-rpmforge-testing
       enabled = 0
       protect = 0
       gpgkey = file:///etc/pki/rpm-gpg/RPM-GPG-KEY-rpmforge-dag
       gpgcheck = 1
       EOF
       ```

更新软件包缓存

```bash
sudo yum makecache
```
