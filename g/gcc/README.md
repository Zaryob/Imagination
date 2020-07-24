GCC Image
---------

![Automation Status](https://img.shields.io/docker/cloud/automated/zaryob/gcc?logo=docker&style=flat-square)
![Docker Status](https://img.shields.io/docker/cloud/build/zaryob/gcc?logo=docker&style=flat-square)

This is specs for GCC Images.

There are two tags in this folder each of them is a new image:

* musl: Alpine based gcc updated image. It uses gcc package of Alpine.
![Musl Container](https://img.shields.io/docker/image-size/zaryob/gcc/musl?color=green&label=%22musl%22%20image%20size&logo=codesandbox)

* glibc: Building is under construction.
![Glibc Container](https://img.shields.io/docker/image-size/zaryob/gcc/glibc?color=green&label=%22glibc%22%20image%20size&logo=codesandbox)


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
