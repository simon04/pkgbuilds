# auto-generated by nodejs-npm2arch
# yaourt -S nodejs-npm2arch
_npmname=webpack
_npmver=3.0.0
pkgname=nodejs-webpack # All lowercase
pkgver=3.0.0
pkgrel=1
pkgdesc="Packs CommonJs/AMD modules for the browser. Support loaders to preprocess json, jsx, es7, css, less files"
arch=(any)
url="http://github.com/webpack/webpack"
license=(MIT)
depends=('nodejs')
optdepends=()
makedepends=('npm')
source=(http://registry.npmjs.org/$_npmname/-/$_npmname-$_npmver.tgz)
noextract=($_npmname-$_npmver.tgz)
sha256sums=('290be3ffe1210b09e057afdc062e80ad6c6041d43ecc26dc4d525871eb1900e0')

package() {
  cd $srcdir
  local _npmdir="$pkgdir/usr/lib/node_modules/"
  mkdir -p $_npmdir
  cd $_npmdir
  npm install -g --prefix "$pkgdir/usr" $_npmname@$_npmver
}

# vim:set ts=2 sw=2 et:
