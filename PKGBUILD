# Maintainer: Ricard Lado <ricard@lado.one>

pkgname=oink
pkgver=1.3.1
pkgrel=1
pkgdesc='A lightweight DDNS client for Porkbun'
arch=(x86_64)
url='https://github.com/RLado/Oink'
license=('MIT')
depends=('glibc')
makedepends=('go')
backup=(etc/oink_ddns/config.json)
source=("https://github.com/RLado/Oink/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('8fc5ecb3493f9879547764e3e1eee37ae128b1bd803831ddc8ac198d2dd13aba')

build() {
	cd "Oink-${pkgver}"
	make
}

package() {
	cd "Oink-${pkgver}"
	make DESTDIR="${pkgdir}/" install
}

