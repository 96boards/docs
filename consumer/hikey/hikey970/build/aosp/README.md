---
title: Build AOSP on HiKey970
permalink: /documentation/consumer/hikey/hikey970/build/aosp/
redirect_from: /documentation/consumer/hikey970/build/aosp/
---

# Build AOSP for HiKey970

# Build preparation

The following instructions can be used to attempt a build based on the AOSP master branch. Other branches (such as stable/release branches are not supported).

In this page, we assume that `<ANDROID_TOP>` is the top level folder for your Android environment. e.g.:
```shell
$ mkdir <ANDROID_TOP>
$ cd <ANDROID_TOP>
```
Then run:
```shell
$ repo init -u https://android.googlesource.com/platform/manifest -b master
$ git clone https://github.com/96boards-hikey/android-manifest.git -b hikey970_v1.0 .repo/local_manifests
$ repo sync -j$(nproc) -c
$ source build/envsetup.sh
$ lunch hikey970-userdebug
```
It might take quite a bit of time to fetch the entire AOSP source code!

# Copy Pre-Built Kernel Binaries

- [Build the Kernel](./linux-kernel/)

- Copy kirin970-hikey970.dtb.dtb (kernel/hikey-linaro/arch/arm64/boot/dts/hisilicon/ kirin970-hikey970.dtb) to the device/linaro/hikey-kernel directory as file: kirin970-hikey970.dtb-4.9

- Copy the Image file (kernel/hikey-linaro/arch/arm64/boot/Image.gz-dtb) to the device/linaro/hikey-kernel directory as file: Image.gz-hikey970-4.9

# Building AOSP
```shell
$ make -j$(nproc)
```

# Installation

- Proceed to [Installation Instructions](../installation)
