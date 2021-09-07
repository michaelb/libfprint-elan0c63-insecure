# libfprint-elan0c63-insecure

This is a libfprint copy with some tweaks\* and (ugly) hacks to make the fingerprint scanner actually usable.

Is it really insecure ?
Not really, so far my rates are:

- False positive (insecure) : 0%
- False negative (inconvenient) : 20%

but I've only tested this with my own fingers and device.

Require fprintd 1.92.0  or ealier, 1.94.0 breaks something

\* from Tuxedo dev Werner Sembach, see [related gitlab MR](https://gitlab.freedesktop.org/libfprint/libfprint/-/merge_requests/198)


## Installation

Choose either method

Precompiled (Arch only):
- download the libfprintxxxx.pkg.tar.zst from the last release
- sudo pacman -U libfprint-xxxxx.pkg.tar.zst


<br/>
<br/>

Package+compile yourself:
- git clone https://github.com/michaelb/libfprint-elan0c63-insecure.git

OR
- download the provided PKGBUILD individually

then

- makepkg -i


<br/>
<br/>

Full manual:
- sudo pacman -S git meson gtk-doc gobject-introspection      # install the build dependencies:
- git clone https://github.com/michaelb/libfprint-elan0c63-insecure.git
- cd libfprint-elan0c63-insecure
- git checkout v1.92.1.r2insecure #or the last release
- meson build
- cd build
- meson compile
- use the compiled library in your system somehow, if you're here you know what you're doing (right?)


