Rust Image
----------

![Automation Status](https://img.shields.io/docker/cloud/automated/zaryob/gcc?logo=docker&style=flat-square)
![Docker Status](https://img.shields.io/docker/cloud/build/zaryob/gcc?logo=docker&style=flat-square)

This is specs for GCC Images.

There are two tags in this folder each of them is a new image:

* *latest*: ![Latest Container](https://img.shields.io/docker/image-size/zaryob/rust/latest?color=green&label=%22latest%22%20image%20size&logo=codesandbox) Alpine based rust updated image.

* *nightly_musl*: ![Nightly Musl Container](https://img.shields.io/docker/image-size/zaryob/rust/nightly_musl?color=green&label=%22nightly_musl%22%20image%20size&logo=codesandbox) Alpine used image. Image generated with rustup script. Toolchain is set as nightly.

* *nightly_glibc*: ![Nightly Glibc Container](https://img.shields.io/docker/image-size/zaryob/rust/nightly_glibc?color=green&label=%22nightly_glibc%22%20image%20size&logo=codesandbox) Alpine used image. Image generated with rustup script. Toolchain is set as nightly.

* *stable_musl*: ![Stable Musl Container](https://img.shields.io/docker/image-size/zaryob/rust/stable_musl?color=green&label=%22stable_musl%22%20image%20size&logo=codesandbox) Alpine used image. Image generated with rustup script. Toolchain is set as stable.

* *stable_glibc*: ![Stable Musl Container](https://img.shields.io/docker/image-size/zaryob/rust/stable_glibc?color=green&label=%22stable_glibc%22%20image%20size&logo=codesandbox) Alpine used image. Image generated with rustup script. Toolchain is set as stable.

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
