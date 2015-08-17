# Contributor: Anton Shestakov <engored*ya.ru>
# Maintainer: listx <linusarver <at> gmail <dot> com>
# This PKGBUILD lives at https://github.com/listx/aurpkgs

pkgname=sdlmame-cheats
pkgver=0.156
pkgrel=1
_srcver=0156
pkgdesc='Official XML Cheat Collection for MAME. For use with sdlmame.'
url='http://www.mamecheat.co.uk/'
license=('unknown')
arch=('any')
depends=('sdlmame>=0.145u1') # XML cheat engine since 0.127, 7z support since 0.145u1
optdepends=("sdlmame>=$pkgver: this package is best used with an up-to-date version of sdlmame.")
makedepends=('unzip')
source=("http://cheat.retrogames.com/download/cheat${_srcver}.zip")
install=sdlmame-cheats.install
sha1sums=('5bd97c20c6390c63bcb98a22a8cbfd98d9561ada')

build() {
  unzip -of "cheat${_srcver}.zip"
}

package() {
  install -Dm644 cheat.7z "$pkgdir/usr/share/sdlmame/cheat.7z"
  install -Dm644 cheat.txt "$pkgdir/usr/share/doc/sdlmame-cheats/cheat.txt"
  install -Dm644 "!README_FIRST!!.txt" "$pkgdir/usr/share/doc/sdlmame-cheats/!README_FIRST!!.txt"
}
