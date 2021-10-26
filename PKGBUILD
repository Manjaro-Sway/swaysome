# Maintainer: Jonas Strasel <info@jonas-strassel.de>

pkgname="swaysome"
pkgver=1.1.2
pkgrel=1
pkgdesc="This binary helps you configure sway to work a bit more like Awesome. This currently means workspaces that are name-spaced on a per-screen basis." 
arch=("x86_64" "aarch64")
url="https://gitlab.com/hyask/$pkgname"
license=("none")
makedepends=("rust" "cargo" "git")
_commit="60fdf90d4d4ab075b4eb4121c09ea9ef855df109"
source=("$pkgname-$pkgver.tar.gz::$url/-/archive/$pkgver/$pkgname-$pkgver.tar.gz")
sha256sums=('f7bc20ff45edb683b87b86bb1213d4940c512a38ab939e76882f9273f0917861')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    cargo build --release --locked 
}

package() {
    install -D -m755 "$srcdir/$pkgname-$pkgver/target/release/$pkgname" "$pkgdir/usr/bin/$pkgname"
    install -D -m644 "$srcdir/$pkgname-$pkgver/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
