# zfs

## Description

This repository contains spec files for building `zfs` RPM packages.

Packages are built and published by [spec-package-builder](https://github.com/damex-el-packages/spec-package-builder) pipeline.

Currently, packages and their corresponding spec files are built and tested only for `Red Hat Enterprise Linux 9`, `Red Hat Enterprise Linux 10` and its derivatives like `Alma Linux 9`, `Alma Linux 10`, `Rocky Linux 9` and `Rocky Linux 10`.

[Follow here if you want to use prebuilt packages](#Using-prebuilt-packages).

## Using prebuilt packages

### Add damex-zfs repository with prebuilt packages

To add `damex-zfs` repository to `Red Hat Enterprise Linux 9` install the following package:

```sh
# x86_64
https://yum-repositories.damex.org/zfs/el/9/x86_64/damex-zfs-release-0.2.0-1.el9.x86_64.rpm
# aarch64
https://yum-repositories.damex.org/zfs/el/9/aarch64/damex-zfs-release-0.2.0-1.el9.aarch64.rpm
```

To add `damex-zfs` repository to `Red Hat Enterprise Linux 10` install the following package:

```sh
# x86_64
https://yum-repositories.damex.org/zfs/el/10/x86_64/damex-zfs-release-0.2.0-1.el10.x86_64.rpm
# aarch64
https://yum-repositories.damex.org/zfs/el/10/aarch64/damex-zfs-release-0.2.0-1.el10.aarch64.rpm
```

Alternatively, it can be done manually by adding the following configuration to `/etc/yum.repos.d/damex-zfs.repo`:

```sh
[damex-zfs]
name = damex-zfs
baseurl = https://yum-repositories.damex.org/zfs/el/$releasever/$basearch
gpgcheck = 1
repo_gpgcheck = 1
gpgkey = https://yum-repositories.damex.org/zfs/zfs-2036-09-25.asc
```

### List of prebuilt packages

| Package              | Repository | Architecture | Distributives              |
|----------------------|------------|--------------|----------------------------|
| zfs                  | damex-zfs | x86_64, aarch64 | Red Hat Enterprise Linux 9, Red Hat Enterprise Linux 10 |
| zfs-devel            | damex-zfs | x86_64, aarch64 | Red Hat Enterprise Linux 9, Red Hat Enterprise Linux 10 |
| zfs-dkms             | damex-zfs | x86_64, aarch64 | Red Hat Enterprise Linux 9, Red Hat Enterprise Linux 10 |
| zfs-dracut           | damex-zfs | x86_64, aarch64 | Red Hat Enterprise Linux 9, Red Hat Enterprise Linux 10 |
| zfs-libs             | damex-zfs | x86_64, aarch64 | Red Hat Enterprise Linux 9, Red Hat Enterprise Linux 10 |
| zfs-pam              | damex-zfs | x86_64, aarch64 | Red Hat Enterprise Linux 9, Red Hat Enterprise Linux 10 |
