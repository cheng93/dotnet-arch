# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=dotnet-arch
pkgver=9.0.100
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
source=("https://download.visualstudio.microsoft.com/download/pr/308f16a9-2ecf-4a42-b8bb-c1233de985fd/be6e87045ab21935bd8bb98ce69026c4/${_pkgdir}.tar.gz")
sha512sums=("7f69bda047de1f952286be330a5e858171ded952d1aa24169e62212f90a27149e63b636c88ad313a6e3ec860da31f8c547ff4ab6808103a070f7fb26ba99c1c7")

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
