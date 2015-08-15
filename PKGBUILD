# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=gameclock
pkgname=gameclock
pkgver=1.0.4
pkgrel=3
pkgdesc="Game clock that shows two analog clock faces"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-cairo' 'haskell-containers=0.3.0.0' 'haskell-glib' 'haskell-gtk' 'haskell-time=1.1.4')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('f4cfe993331d57cc058a0cd102410ca8')
