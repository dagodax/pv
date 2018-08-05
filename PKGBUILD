pkgname=pv
pkgver=1.6.6
pkgrel=1
pkgdesc='A terminal-based tool for monitoring the progress of data through a pipeline.'
arch=('x86_64')
url='http://www.ivarch.com/programs/pv.shtml'
license=('custom:Artistic 2.0')
depends=('glibc')
source=("http://www.ivarch.com/programs/sources/$pkgname-$pkgver.tar.bz2")
md5sums=('ff3564fddcc2b9bd4a9c1d143aba4b4c')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  ./configure --prefix=/usr --mandir=/usr/share/man
  make
}
  
package() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  make DESTDIR="$pkgdir" install
  install -Dm0644 doc/COPYING "$pkgdir/usr/share/licenses/$pkgname/COPYING"
}
