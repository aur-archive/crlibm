# Maintainer: Nicolas Stalder <nicolas dot stalder at gmail dot com>
pkgname=crlibm
pkgver=1.0beta4
pkgrel=2
epoch=
pkgdesc="CRlibm, an efficient and proven correctly-rounded mathematical library."
arch=('x86_64')
url="http://lipforge.ens-lyon.fr/www/crlibm/"
license=('LGPL')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(http://lipforge.ens-lyon.fr/frs/download.php/162/$pkgname-$pkgver.tar.gz)
noextract=()
md5sums=('8ecabd55d4a2d08030eb770ae2a5670a')


build() {
  cd "$srcdir/$pkgname-$pkgver"
  CFLAGS=-fPIC LDFLAGS=-fPIC ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
  install -Dm644 COPYING.LIB $pkgdir/usr/share/licenses/crlibm/LICENSE
}

# vim:set ts=2 sw=2 et:
