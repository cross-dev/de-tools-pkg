# Maintainer: Roman Saveljev <roman.saveljev@haltian.com>
pkgname=de-tools
pkgver=1.0.0
pkgrel=1
epoch=
pkgdesc="Tools package for both development and integration environments"
arch=('any')
url="https://github.com/cross-dev/de-tools"
license=('MIT')
groups=()
depends=('perl')
makedepends=()
checkdepends=('bats-git')
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/cross-dev/${pkgname}/archive/${pkgver}.tar.gz"
       )
noextract=()
md5sums=('9d93fd05005715ba5dd9ecfbee41ad3b')
validpgpkeys=()

prepare() {
	: cd "$pkgname-$pkgver"
	: patch -p1 -i "$srcdir/$pkgname-$pkgver.patch"
}

build() {
	cd "$pkgname-$pkgver"
	make
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}
