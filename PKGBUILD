# Maintainer: Riel Joseph <bulaybulay.rielj@gmail.com>
pkgname=golings
pkgver=0.6.2
pkgrel=1
pkgdesc="Rustlings for Golang this time"
arch=('x86_64')
url="https://github.com/mauricioabreu/golings"
license=('APACHE')
depends=('go')
provides=("golings")
conflicts=("golings")
install="golings.install"
source=("${pkgname}-${pkgver}::git+https://github.com/mauricioabreu/golings.git#tag=v${pkgver}")
md5sums=('SKIP') 

build() {
  cd ${pkgname}-${pkgver}/golings
  go build -o ${srcdir}/golings
}

package() {
  cd ${srcdir}
  install -D golings -t "$pkgdir"/usr/bin/
  cd ${pkgname}-${pkgver}
  install -Dm 644 README.md -t "$pkgdir"/usr/share/doc/$pkgname
  install -Dm 644 LICENSE -t "$pkgdir"/usr/share/licenses/$pkgname
}


