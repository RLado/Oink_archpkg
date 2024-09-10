# Maintainer: Ricard Lado <ricard@lado.one>

pkgname=oink
pkgver=1.3.0
pkgrel=1
pkgdesc='A lightweight DDNS client for Porkbun'
arch=(x86_64)
url='https://github.com/RLado/Oink'
license=('MIT')
depends=('glibc')
makedepends=('go')
backup=(etc/oink_ddns/config.json)
source=("https://github.com/RLado/Oink/archive/refs/tags/v${pkgver}.tar.gz")
sha256sums=('6a58cdd8263a76872635cd3e2fd1d6f1932508cd3de8ec22f7300a7390a2b18e')

build() {
	cd "Oink-${pkgver}"
	make
}

package() {
	cd "Oink-${pkgver}"
	make DESTDIR="${pkgdir}/" install
}

