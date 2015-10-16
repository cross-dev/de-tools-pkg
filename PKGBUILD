# Maintainer: Roman Saveljev <roman.saveljev@haltian.com>
pkgname=de-tools
pkgver=1.0.1
pkgrel=1
pkgdesc="Tools package for both development and integration environments"
arch=('any')
url="https://github.com/cross-dev/de-tools"
license=('MIT')
depends=('perl')
checkdepends=('bats-git')
source=("https://github.com/cross-dev/${pkgname}/archive/${pkgver}.tar.gz"
       )
md5sums=('d12a9a2212e8e3aa030fcf9297e2e45c')

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
