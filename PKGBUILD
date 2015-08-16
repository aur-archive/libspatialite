# Maintainer: Brian Galey <bkgaley at gmail dot com>
# Contributor: Pietro Zambelli <peter.zamb at gmail dot com>
pkgname=libspatialite
pkgver=4.1.1
pkgrel=3
pkgdesc="SQLite extension to support spatial data types and operations"
arch=('i686' 'x86_64')
url="https://www.gaia-gis.it/fossil/libspatialite/index"
license=('MPL')
depends=('geos' 'libfreexl' 'libxml2' 'proj' 'sqlite3' 'zlib')
options=('!libtool')
source=("http://www.gaia-gis.it/gaia-sins/$pkgname-sources/$pkgname-$pkgver.tar.gz")
sha256sums=('0481a20af952f4a38c9dbb10f37fd38c45f16c50397f8da0079e02435b9b910f')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr \
    --enable-libxml2
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}
