# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=dotnet-arch
pkgver=8.0.203
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
source=("https://download.visualstudio.microsoft.com/download/pr/656a3402-6889-400f-927f-7f956856e58b/93750973d6eedd17c6d963658e7ec214/${_pkgdir}.tar.gz")
sha512sums=("78b1913b54a1a4c9f13cc2864a11540b5fd3bdf4ebb49837483e19c0906a1890f2dfcf173635a1c89714bf735cbcaa01db0f7ae90add5295da69a0638ed5e60e")

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
