# Maintainer: Michael Riegert <michael at eowyn net>
# Maintainer: Scott Shawcroft <scott at tannewt dot org>

pkgname=oss-cad-suite-build-bin
_pkgver=2022-12-14
pkgver=${_pkgver//-/}
pkgrel=1
pkgdesc="Nightly builds of open-source FPGA tools"
arch=('x86_64' 'arm' 'aarch64')
url="https://github.com/YosysHQ/oss-cad-suite-build"
license=('custom')

source_x86_64=($url/releases/download/$_pkgver/oss-cad-suite-linux-x64-$pkgver.tgz)
#source_arm=($url/releases/download/$_pkgver/oss-cad-suite-linux-arm-$pkgver.tgz)
#source_aarch64=($url/releases/download/$_pkgver/oss-cad-suite-linux-arm64-$pkgver.tgz)
#sha256sums=('SKIP')
sha256sums_x86_64=('80f992bc58ab82b9854838cb1443bece8fc2306b02e99e807b2d979b0ac53c60')
#sha256sums_arm=('SKIP')
#sha256sums_aarch64=('SKIP')

replaces=('fpga-toolchain-bin')

package() {
    rsync -a "$srcdir/oss-cad-suite" "$pkgdir/opt/" --chmod=755 --exclude README --exclude license
    mkdir -p "$pkgdir/usr/share/licenses/oss-cad-suite-build/"
    cp "$srcdir/oss-cad-suite/license/"* "$pkgdir/usr/share/licenses/oss-cad-suite-build/"
}
