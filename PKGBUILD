pkgname=darwin
pkgver="$(date +%Y%m%d)"
pkgrel=1
pkgdesc='Darwin - a font family optimized for academic, scientific, and book writing'
url='https://darwintypeface.com/'
arch=('i686' 'x86_64')
license=('OFL-1.1')
depends=()
makedepends=()

provides=('darwin')

build() {
  cd "${srcdir}"
  rm -fr build; cp -a "${startdir}"/output build
  cp "${startdir}"/LICENSE.md build
}

package() {
  cd "${srcdir}/build"
  install -Dm644 'DarwinSerif-Regular.otf' "${pkgdir}/usr/share/fonts/OTF/DarwinSerif-Regular.otf"
  install -Dm644 'DarwinSerif-Regular.ttf' "${pkgdir}/usr/share/fonts/TTF/DarwinSerif-Regular.ttf"
  install -Dm644 'LICENSE.md' "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.md"
}

