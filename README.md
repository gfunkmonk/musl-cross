# musl-cross

This is a simple, lightweight project for making cross-compilation toolchain with musl libc.

## Supported targets

| Target                           | Kernel | Binutils | GCC    | Musl  | Mold   |
|----------------------------------|--------|----------|--------|-------|--------|
| aarch64-unknown-linux-musl       | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| aarch64_be-unknown-linux-musl    | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| arm-unknown-linux-musleabi       | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| arm-unknown-linux-musleabihf     | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| armv5-unknown-linux-musleabi     | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| armv6-unknown-linux-musleabi     | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| armv6-unknown-linux-musleabihf   | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| armv7-unknown-linux-musleabi     | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| armv7-unknown-linux-musleabihf   | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| i386-unknown-linux-musl          | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| i486-unknown-linux-musl          | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| i586-unknown-linux-musl          | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| i686-unknown-linux-musl          | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| loongarch64-unknown-linux-musl   | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| m68k-unknown-linux-musl          | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| microblaze-xilinx-linux-musl     | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| microblazeel-xilinx-linux-musl   | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| mips-unknown-linux-musl          | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| mips-unknown-linux-muslsf        | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| mips64-unknown-linux-musl        | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| mips64el-unknown-linux-musl      | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| mipsel-unknown-linux-musl        | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| mipsel-unknown-linux-muslsf      | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| or1k-unknown-linux-musl          | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | N/A    |
| powerpc-unknown-linux-musl       | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| powerpc-unknown-linux-muslsf     | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| powerpc64-unknown-linux-musl     | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| powerpc64le-unknown-linux-musl   | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| powerpcle-unknown-linux-musl     | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| powerpcle-unknown-linux-muslsf   | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| riscv32-unknown-linux-musl       | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| riscv64-unknown-linux-musl       | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| s390x-ibm-linux-musl             | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| sh4-multilib-linux-musl          | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |
| x86_64-unknown-linux-musl        | 6.18.41   | 2.46  | 16.2.0 | 1.2.6 | 2.41.0 |

## How to use

Download the tarball from the [release page](https://github.com/cross-tools/musl-cross/releases) and extract it to `/opt/x-tools`:

```sh
sudo mkdir -p /opt/x-tools
sudo tar -xf ${target}.tar.xz -C /opt/x-tools
```

## How to build

Fork this project and create a new release, or build manually:

```sh
./scripts/make ${target}
```

## License

MIT

## Acknowledgements

We would like to express our gratitude to the following individuals and projects:

- [crosstool-ng](https://github.com/crosstool-ng/crosstool-ng)
- [musl-libc](https://musl.libc.org)
