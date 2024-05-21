# Maintainer: Eric TK <ericatkusa@gmail.com>
pkgname=clearch-cli
pkgver=0.1.0
pkgrel=1
pkgdesc="A simple CLI tool written in Rust"
arch=('x86_64')
url="https://github.com/Zane-Dev14/ClearchOnlyTar"
license=('MIT')
depends=('glibc')
makedepends=('rust' 'cargo')
source=("https://github.com/Zane-Dev14/ClearchOnlyTar/raw/main/clearch-cli-0.1.0.tar.gz")
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
