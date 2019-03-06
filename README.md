# Microsemi Ocelot Buildroot External

This [external buildroot layer][1] provides a basic support package for the
Microsemi VSC7514EV eval board. This project provides an extension to buildroot to
provide this BSP outside of the standard buildroot tree.

## Build

You have to clone buildroot and this layer. When building, use the
appropriate defconfig in the `buildroot-external-mscc-ocelot/configs`
directory.

```
git clone git://git.busybox.net/buildroot -b 2019.02
git clone https://github.com/kontron/buildroot-external-mscc-ocelot
mkdir build
cd build
make BR2_EXTERNAL=../buildroot-external-mscc-ocelot O=`pwd` -C ../buildroot mscc_ocelot_defconfig
make
```

[1]: https://buildroot.org/downloads/manual/manual.html#outside-br-custom
