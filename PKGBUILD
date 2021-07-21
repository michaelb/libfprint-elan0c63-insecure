# Maintainer: Michael Bleuez <michael.bleuez2@gmail.com>

pkgname=libfprint-elan0c63-insecure
_pkgname=libfprint-elan0c63-insecure
epoch=1
pkgver=1.92.1.r2insecure
pkgrel=1
pkgdesc="Copy of libfprint, with (probably insecure) tweaks so elan 0c63 gets actually usable"
url="https://github.com/michaelb/libfprint-elan0c63-insecure"
arch=(x86_64)
license=(LGPL)
depends=(libgusb pixman nss systemd-libs)
makedepends=(git meson gtk-doc gobject-introspection systemd)
provides=("libfprint=$pkgver" libfprint-2.so)
conflicts=(libfprint)
groups=(fprint)
source=("git+https://github.com/michaelb/libfprint-elan0c63-insecure.git")
sha256sums=('SKIP')

pkgver() {
  cd $_pkgname
  git describe --tags | sed 's/^V_\|^v//;s/_/./g;s/-/.r/;s/-/./'
}

prepare() {
  cd $_pkgname
}

build() {
  arch-meson $_pkgname build
  meson compile -C build
}


package() {
  DESTDIR="$pkgdir" meson install -C build
}
