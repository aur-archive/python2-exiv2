# Maintainer : Martin Wimpress <code@flexion.org>
# Contributor: Archie <xMickael@ifrance.com>
# Contributor: Byron Clark <byron@theclarkfamily.name>


_pkgname=pyexiv2
pkgname=python2-exiv2
pkgver=0.3.2
pkgrel=2
pkgdesc="pyexiv2 is a Python binding to exiv2, the C++ library for manipulation of EXIF, IPTC and XMP image metadata."
depends=('python2' 'boost-libs' 'exiv2')
makedepends=('scons' 'boost')
replaces=('pyexiv2')
conflicts=('pyexiv2')
provides=('pyexiv2')
arch=('i686' 'x86_64' 'armv6h' 'armv7h')
license=('GPL')
source=(http://launchpad.net/${_pkgname}/0.3.x/${pkgver}/+download/${_pkgname}-${pkgver}.tar.bz2)
md5sums=('9c0377ca4cf7d5ceeee994af0b5536ae')
url="http://tilloy.net/dev/pyexiv2"

build() {
    cd ${srcdir}/${_pkgname}-${pkgver}
    scons
}

package() {
    cd ${srcdir}/${_pkgname}-${pkgver}
    scons DESTDIR=${pkgdir} install
}
