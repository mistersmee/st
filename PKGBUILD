# Maintainer:

pkgname=st-aseem
_pkgname=st
pkgver=1.4.r129.22678d4
pkgrel=1
epoch=1
pkgdesc="My build of st."
url='https://github.com/mistersmee/st'
arch=(any)
license=('MIT')
depends=('git')
makedepends=('make')
source=('git://github.com/mistersmee/st')
sha1sums=('SKIP')

provides=("${_pkgname}")
conflicts=("${_pkgname}")

pkgver() {
	cd "${_pkgname}"
	printf "%s.r%s.%s" "$(awk '/^VERSION =/ {print $3}' config.mk)" \
		"$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

prepare() {
	cd $srcdir/${_pkgname}
}

build() {
	cd "${_pkgname}"
	make
}

package() {
	cd "${_pkgname}"
	make PREFIX=/usr DESTDIR="${pkgdir}" install
}
