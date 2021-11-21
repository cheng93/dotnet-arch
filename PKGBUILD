# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=dotnet-arch
pkgver=6.0.100
pkgrel=1
arch=('x86_64')
url=https://www.microsoft.com/net/core
license=(MIT)
makedepends=(
  icu
  openssl-1.0
)
options=(staticlibs)
_pkgdir="dotnet-sdk-${pkgver}-linux-x64"
source=("https://download.visualstudio.microsoft.com/download/pr/17b6759f-1af0-41bc-ab12-209ba0377779/e8d02195dbf1434b940e0f05ae086453/${_pkgdir}.tar.gz")
sha512sums=("cb0d174a79d6294c302261b645dba6a479da8f7cf6c1fe15ae6998bc09c5e0baec810822f9e0104e84b0efd51fdc0333306cb2a0a6fcdbaf515a8ad8cf1af25b")

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
