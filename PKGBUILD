# Maintainer: Antonio Rojas <arojas@archlinux.org>
# Contributor: Jan de Groot <jgc@archlinux.org>

pkgname=minimal-iso-codes
pkgver=4.20.1
pkgrel=1
pkgdesc='Lists of the country, language, and currency names'
url='https://github.com/removed-user/minimal-iso-codes'
arch=(any)
license=(LGPL-2.1-only)

provides=(minimal-iso-codes iso-codes )
conflicts=(iso-codes)

makedepends=(
git
meson
python
)

#source=(git+https://github.com/removed-user/minimal-iso-codes)
#source=(git+https://github.com/removed-user/minimal-iso-codes#tag=v$pkgver)
sha512sums=()

build() {
meson setup build $pkgname --wipe
meson compile -C build
}

package() {
  meson install -C build --destdir="$pkgdir"
}
