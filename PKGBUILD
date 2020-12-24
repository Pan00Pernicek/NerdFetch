# Maintainer: PanPernicek aloushekhlupacek@gmail.com
#i wont maintain this very much
pkgname="rfetch"
pkgver=2
pkgrel=2
pkgdesc="A POSIX fetch"
arch=('any')
optdepends=('bc: memory percent')
url="https://github.com/Pan00Pernicek/rfetch/"
license=('GPL')
makedepends=('git')
source=("git+https://github.com/Pan00Pernicek/rfetch/")
noextract=()
md5sums=('SKIP')

pkgver() {
	cd rfetch
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

prepare() {
	cd rfetch
}

package() {
	install -Dm755 "$srcdir"/rfetch/rfetch "$pkgdir/usr/bin/rfetch"
	install -Dm644 "$srcdir"/rfetch/README.md "$pkgdir/usr/share/doc/$pkgname"
}
