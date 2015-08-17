# Maintainer: Bertrand Bonnefoy-Claudet <bertrandbc@gmail.com>

_gemname=grit
pkgname=ruby-$_gemname-2.5
pkgver=2.5.0
pkgrel=1
pkgdesc="Ruby Git bindings."
arch=('any')
url="http://github.com/mojombo/grit"
license=('MIT')
depends=('ruby' 'ruby-posix-spawn>=0.3.6' 'ruby-mime-types-1.16' 'ruby-diff-lcs>=1.1')
makedepends=('rubygems')
conflicts=('ruby-grit')
source=(http://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
md5sums=('bb66887fe3eb7bfaef50c6b86bbabfc1')
sha1sums=('0581087581cd522a697616b835b4d57f90a90ca6')

package() {
  cd "$srcdir"
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
}

