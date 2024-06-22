# Maintainer: Ricard Lado <ricard@lado.one>

pkgname=oink
pkgver=1.2.0
pkgrel=1
pkgdesc='A lightweight DDNS client for Porkbun'
arch=(x86_64)
url='https://github.com/RLado/Oink'
license=('MIT')
depends=('glibc')
makedepends=('go')
backup=(etc/oink_ddns/config.json)
source=("https://github.com/RLado/Oink/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('6cdfc45cc3ea11784e4d58b025fd9777164d0ca56c9c790940ec9814f3586819')

build() {
	cd "Oink-${pkgver}"
	make
}

package() {
	cd "Oink-${pkgver}"
	make DESTDIR="${pkgdir}/" install
}

