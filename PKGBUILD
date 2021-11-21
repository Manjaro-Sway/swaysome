# Maintainer: Renner03 <Renner03@protonmail.com>

pkgname=swaysome
_pkgname=swaysome
pkgver=1.1.5
pkgrel=1
pkgdesc='AwesomeWM-like workspaces for sway'
arch=("x86_64" "aarch64")
url='https://gitlab.com/hyask/swaysome'
license=('MIT')
makedepends=('git' 'rust')
provides=("$_pkgname")
conflicts=("$_pkgname")
source=("$pkgname-$pkgver.tar.gz::$url/-/archive/$pkgver/$pkgname-$pkgver.tar.gz")
md5sums=('f1d4130aee527c5dd803ac6e118d226a')

build() {
  cd "$_pkgname-$pkgver"
  cargo build --release
}

package() {
  cd "$_pkgname-$pkgver"
  install -Dm755 "target/release/$_pkgname" "$pkgdir/usr/bin/$_pkgname"
}
