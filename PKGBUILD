# Maintainer: Michael Riegert <michael at eowyn net>
# Maintainer: Scott Shawcroft <scott at tannewt dot org>

pkgname=oss-cad-suite-build-bin
_pkgver=2023-01-04
pkgver=${_pkgver//-/}
pkgrel=1
pkgdesc="Nightly builds of open-source FPGA tools"
arch=('x86_64' 'arm' 'aarch64')
url="https://github.com/YosysHQ/oss-cad-suite-build"
license=('custom')

source_x86_64=($url/releases/download/$_pkgver/oss-cad-suite-linux-x64-$pkgver.tgz)
sha256sums_x86_64=('SKIP')

replaces=('fpga-toolchain-bin')

package() {
    cp -r "$srcdir/oss-cad-suite" "$pkgdir/opt/"
    chmod -R 755 "$pkgdir/opt/oss-cad-suite"
    mkdir -p "$pkgdir/usr/share/licenses/oss-cad-suite-build/"
    cp -i "$srcdir/oss-cad-suite/license/"* "$pkgdir/usr/share/licenses/oss-cad-suite-build/"
}
