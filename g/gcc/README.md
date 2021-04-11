GCC Image
---------

![Automation Status](https://img.shields.io/github/workflow/status/Zaryob/Imagination/gcc_build?style=flat-square)
![Docker Status](https://img.shields.io/docker/cloud/build/zaryob/gcc?logo=docker&style=flat-square)
![Docker Pulls](https://img.shields.io/docker/pulls/zaryob/gcc?logo=docker&style=flat-square)
![Docker Stars](https://img.shields.io/docker/stars/zaryob/gcc?logo=docker&style=flat-square)
![Docker Architectures](https://img.shields.io/badge/architectures-amd64%20%7C%20armv7%20%7C%20arm64-blue)

This is specs for GCC Images.

There are two tags in this folder each of them is a new image:

* *musl*: ![Musl Container](https://img.shields.io/docker/image-size/zaryob/gcc/musl?color=green&label=%22musl%22%20image%20size&logo=codesandbox)  Alpine based gcc updated image. It uses gcc package of Alpine.



* *glibc*: ![Glibc Container](https://img.shields.io/docker/image-size/zaryob/gcc/glibc?color=green&label=%22glibc%22%20image%20size&logo=codesandbox) Building is under construction.


**Note:** Latest builded with using glibc.

Usage
-----

For latest/glibc:

```shell
        $ docker run -itd zaryob/gcc
```

For musl:

```shell
        $ docker run -itd zaryob/gcc:musl
```
