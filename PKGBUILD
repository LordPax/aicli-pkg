# Maintainer: teddy gauthier <teddy.gauthier@outlook.com>

pkgname=aicli
pkgver=0.1.0
pkgrel=1
pkgdesc="Projet to use ai api to generate text, image, etc."
arch=(x86_64 i686 armv7h aarch64)
url="https://github.com/LordPax/${pkgname}"
license=(MIT)
depends=()
makedepends=(go)
source=("${url}/archive/refs/tags/v${pkgver}.tar.gz")
md5sums=('3f13ccf73ba9d44f4271d9c7c6810b1d')

build() {
	cd "${pkgname}-${pkgver}"
	go mod download
	go build
}

package() {
	install -Dm755 "${pkgname}-${pkgver}/${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
}
