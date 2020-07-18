# Maintainer: idongliming <idongliming@qq.com>
pkgname=simple_sdl_sanke
pkgver=1.0
pkgrel=1
epoch=
pkgdesc="Simple Snake game developed by SDL"
arch=("x86_64")
url="https://github.com/idongliming/simple-sdl-snake"
license=("MIT")
groups=()
depends=('sdl2' 'sdl2_image' 'sdl2_ttf')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("git+https://github.com/idongliming/simple-sdl-snake")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

build() {
	cd "$srcdir"
	gcc Snake.cpp -o simple-sdl-snake -w -lSDL2main -lSDL2 -lSDL2_ttf -lSDL2_image
}

package() {
	cd "${srcdir}"
    install -dm755 "${pkgdir}/opt/${pkgname}"
    cp simple-sdl-snake ${pkgdir}/opt/simple_sdl_sanke/
    cp -r assets ${pkgdir}/opt/simple_sdl_sanke/

    install -dm755 "${pkgdir}/usr/bin"
    ln -s "/opt/simple_sdl_sanke/simple_sdl_sanke" "${pkgdir}/usr/bin/simple_sdl_sanke"
}
