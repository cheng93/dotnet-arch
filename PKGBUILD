# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=dotnet-arch
pkgver=8.0.101
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
source=("https://download.visualstudio.microsoft.com/download/pr/9454f7dc-b98e-4a64-a96d-4eb08c7b6e66/da76f9c6bc4276332b587b771243ae34/${_pkgdir}.tar.gz")
sha512sums=("26df0151a3a59c4403b52ba0f0df61eaa904110d897be604f19dcaa27d50860c82296733329cb4a3cf20a2c2e518e8f5d5f36dfb7931bf714a45e46b11487c9a")

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
