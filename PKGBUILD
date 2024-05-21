# Maintainer: Eric TK <ericatkusa@gmail.com>
pkgname=clearch-cli
pkgver=0.1.0
pkgrel=1
pkgdesc="A simple CLI tool written in Rust"
arch=('x86_64')
url="https://github.com/Zane-Dev14/ClearchTest"
license=('MIT')
depends=('glibc')
makedepends=('rust' 'cargo')
source=("$pkgname-$pkgver.tar.gz::https://github.com/The-Capstone-Project/Clearch/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('SKIP')

build() {
    cd "$srcdir/$pkgname-$pkgver"
    cargo build --release
}

package() {
    cd "$srcdir/$pkgname-$pkgver"
    install -Dm755 "target/release/$pkgname" "$pkgdir/usr/bin/$pkgname"
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
    install -Dm644 README.md "$pkgdir/usr/share/doc/$pkgname/README.md"
}
