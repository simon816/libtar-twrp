libtar-twrp
===========

This is a patched version of `libtar` to support tar files created by the [TWRP](https://twrp.me/) backup feature.

It is largely unchanged from the original libtar, for which you can find sources at https://repo.or.cz/libtar.git

The original libtar README contains some info for building libtar.

## Building

(see also: README and INSTALL)

You will need autoconf and libtool to run the build script. You'll also need the following libraries to build:

* zlib
* libcap (TWRP addition)
* libselinux (TWRP addition)


Then run these commands:

```
autoreconf --force --install
./configure
make
make install
```

Instead of installing (`make install`), you can run it directly from the root of the repository with `./libtar/libtar`.

## AUR

An Arch user package is available for systems compatible with the Arch User Respository: [libtar-twrp-git](https://aur.archlinux.org/packages/libtar-twrp-git) maintained by @w568w.

Install with a compatible AUR helper, e.g.:
```
yay -S libtar-twrp-git
```

The libtar binary will be installed at `/opt/libtar-twrp/bin/libtar`
