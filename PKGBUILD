# Maintainer: Denis Yulin <delin@delin.pro>

pkgname=warzone2100-beta
_realname=warzone2100
pkgver=3.1.1
_pkgver=3.1.1
pkgrel=1
pkgdesc="3D realtime strategy game on a future Earth - Development version"
url="http://wz2100.net/"
arch=('i686' 'x86_64')
conflicts=('warzone2100' 'warzone2100-git')
provides=('warzone2100')
license=('GPL')
depends=('gettext' 'physfs' 'quesoglc' 'openal' 'libvorbis' 'glew' 'qjson' 'libtheora' 'ttf-dejavu' 'icu' 'mesa')
makedepends=('zip' 'unzip')
source=("http://downloads.sourceforge.net/project/${_realname}/releases/${_pkgver}/${_realname}-${_pkgver}.tar.xz")
md5sums=('0b81a0012098a1310f5351a3ace2021b')

build() {
  cd "${_realname}-${_pkgver}"

  ./configure --prefix=/usr \
    --with-backend=qt \
    --with-distributor=AUR

  make
}

package() {
  cd "${_realname}-${_pkgver}"

  make DESTDIR="${pkgdir}" install
}
