# Maintainer: Roman Saveljev <roman.saveljev@haltian.com>
pkgname=de-tools
pkgver=1.0.0
pkgrel=1
pkgdesc="Tools package for both development and integration environments"
arch=('any')
url="https://github.com/cross-dev/de-tools"
license=('MIT')
depends=('perl')
checkdepends=('bats-git')
source=("https://github.com/cross-dev/${pkgname}/archive/${pkgver}.tar.gz"
       )
md5sums=('9d93fd05005715ba5dd9ecfbee41ad3b')

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
	make DESTDIR="$pkgdir" install
}
