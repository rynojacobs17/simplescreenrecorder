pkgname=simplescreenrecorder
pkgver=0.3.0
pkgrel=1
pkgdesc="A feature-rich screen recorder that supports X11 and OpenGL."
arch=("x86_64")
url="http://www.maartenbaert.be/simplescreenrecorder/"
license=("GPL3")
depends=("qt4" "ffmpeg" "alsa-lib" "libpulse" "jack" "libgl" "glu" "libx11" "libxext" "libxfixes" "libxi")
optdepends=("lib32-simplescreenrecorder: OpenGL recording of 32-bit applications")
makedepends=("git")
source=("git+https://github.com/MaartenBaert/ssr.git#tag=$pkgver")
md5sums=("SKIP")

options=("!libtool")
install=simplescreenrecorder.install

build() {
  cd ssr
  ./configure --prefix=/usr --disable-assert
  make
}
package() {
  cd ssr
  make DESTDIR="$pkgdir" install
}
