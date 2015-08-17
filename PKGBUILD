# Maintainer: Joris Steyn <jorissteyn@gmail.com>
# Contributor: Xemertix <arch88(at)katamail(dot)com>

pkgname=php-pecl-cairo-svn
pkgver=330459
pkgrel=1
pkgdesc="PHP extension for Cairo graphics library"
arch=('i686' 'x86_64')
url="http://pecl.php.net/package/cairo"
license=('PHP')
source=('pecl-cairo::svn+http://svn.php.net/repository/pecl/cairo/trunk')
md5sums=('SKIP')
depends=('php' 'cairo')
makedepends=('svn')

pkgver() {
  cd "$SRCDEST"/pecl-cairo
  svnversion | tr -d [A-z]
}

build() {
  cd "$srcdir"/pecl-cairo

  phpize
  ./configure
  make
}

package() {
  cd "$srcdir"/pecl-cairo
  make INSTALL_ROOT="$pkgdir/" install
}

