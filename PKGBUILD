# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=dotnet-arch
pkgver=9.0.201
pkgrel=1
arch=('x86_64')
url=https://www.microsoft.com/net/core
license=(MIT)
makedepends=(
  icu
  openssl
)
options=(staticlibs)
_pkgdir="dotnet-sdk-${pkgver}-linux-x64"
source=("https://download.visualstudio.microsoft.com/download/pr/82a7fc96-b53b-4af4-ac3a-ef0a6c9325d5/84e522c31482538cddf696d03c5b20af/${_pkgdir}.tar.gz")
sha512sums=("93a8084ef38da810c3c96504c20ea2020a6b755b73a19f7acc6cd73a8b62ace0adda14452d11e6458f73dc7d58ffad22fcd151f111d2320cb23a10fd54dcb772")

# prepare() {}
# build() {}
# check() {}

package() {
    install -dm 755 "${pkgdir}"{/opt/dotnet,/usr/bin}
    #cp -R ${srcdir}/* "${pkgdir}"/opt/dotnet
    #rm "${pkgdir}"/opt/dotnet/"${_pkgdir}.tar.gz" 
    tar -C "${pkgdir}"/opt/dotnet -xf  "${_pkgdir}.tar.gz" 
    chown -R root:root "${pkgdir}"/opt/dotnet
    ln -s /opt/dotnet/dotnet "${pkgdir}"/usr/bin/dotnet
}
