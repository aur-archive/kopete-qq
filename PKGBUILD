# Maintainer: Kuso Wei <p0ckty@gmail.com>

pkgname=kopete-qq
_gitname=kopete-qq
_gitver='commit=6815326ffb6e31d0f6d73fa8c28af74e3e2508d6'
pkgver=1.0
pkgrel=1
pkgdesc="This is a QQ's kopete plugin, using lwqq library: https://github.com/xiehuc/lwqq."
arch=('i686' 'x86_64')
url="http://kde-apps.org/content/show.php/Kopete+QQ?content=163953"
license=('GPL3')
depends=('kdenetwork-kopete' 'libev' 'js185')
makedepends=('git' 'cmake' 'automoc4')
source=("git://git.oschina.net/zhjun5337/kopete-qq.git#$_gitver")
md5sums=('SKIP')

build() {
  cd "$srcdir/$_gitname"
  mkdir build && cd build
  cmake -DCMAKE_INSTALL_PREFIX=/usr ..
  make
}

package()
{
  cd "$srcdir/$_gitname/build"
  make DESTDIR="$pkgdir" install
}
