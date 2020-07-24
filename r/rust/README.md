Rust Image
----------

![Automation Status](https://img.shields.io/docker/cloud/automated/zaryob/gcc?logo=docker&style=flat-square)
![Docker Status](https://img.shields.io/docker/cloud/build/zaryob/gcc?logo=docker&style=flat-square)

This is specs for GCC Images.

There are two tags in this folder each of them is a new image:

* latest: Alpine based rust updated image.
![Latest Container](https://img.shields.io/docker/image-size/zaryob/rust/latest?color=green&label=%22latest%22%20image%20size&logo=codesandbox)

* nightly_musl: Alpine used image. Image generated with rustup script. Toolchain is set as nightly.
![Nightly Musl Container](https://img.shields.io/docker/image-size/zaryob/rust/nightly_musl?color=green&label=%22nightly_musl%22%20image%20size&logo=codesandbox)

* nightly_glibc: Alpine used image. Image generated with rustup script. Toolchain is set as nightly.
![Nightly Glibc Container](https://img.shields.io/docker/image-size/zaryob/rust/nightly_glibc?color=green&label=%22nightly_glibc%22%20image%20size&logo=codesandbox)

* stable_musl: Alpine used image. Image generated with rustup script. Toolchain is set as stable.
![Stable Musl Container](https://img.shields.io/docker/image-size/zaryob/rust/stable_musl?color=green&label=%22stable_musl%22%20image%20size&logo=codesandbox)

* stable_glibc: Alpine used image. Image generated with rustup script. Toolchain is set as stable.
![Stable Musl Container](https://img.shields.io/docker/image-size/zaryob/rust/stable_glibc?color=green&label=%22stable_glibc%22%20image%20size&logo=codesandbox)

Usage
-----

For latest:

```shell
        $ docker run -itd zaryob/rust
```

For nightly:

```shell
        $ docker run -itd zaryob/rust:nightly_glibc
        # or
        $ docker run -itd zaryob/rust:nightly_musl
```

For stable:

```shell
        $ docker run -itd zaryob/rust:stable_glibc
        # or
        $ docker run -itd zaryob/rust:stable_musl
```
