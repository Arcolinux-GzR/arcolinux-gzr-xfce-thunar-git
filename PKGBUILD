# Maintainer: Erik Dubois <erik.dubois@gmail.com>
# GZ-Maintainer: John Brewer <nytesblood@gmail.com>
pkgname=arcolinux-gzr-xfce-thunar-git
_pkgname=arcolinux-gzr-xfce-thunar
_destname1="/etc/skel/.config/Thunar/"
_destname2="/etc/skel/.config/xfce4/"
_licensedir="/usr/share/arcolinux/licenses/"
pkgver=18.11
pkgrel=1
pkgdesc="xfce-thunar configs from arcolinux customized for GZ"
arch=('any')
url="https://github.com/Arcolinux-GzR/arcolinux-gzr-xfce-thunar"
license=('GPL3')
makedepends=('git')
depends=()
provides=("${pkgname}")
options=(!strip !emptydirs)
source=(${_pkgname}::"git+https://github.com/Arcolinux-GzR/${_pkgname}.git")
sha256sums=('SKIP')
install='readme.install'
package() {
	rm -f "${srcdir}/${_pkgname}/"README.md
	rm -f "${srcdir}/${_pkgname}/"git-v*
	mkdir -p "${pkgdir}${_licensedir}${_pkgname}"
	mv "${srcdir}/${_pkgname}/"LICENSE "${pkgdir}${_licensedir}${_pkgname}/LICENSE"
	mkdir -p "${pkgdir}${_destname1}"
	cp -r "${srcdir}/${_pkgname}/Thunar/"* "${pkgdir}${_destname1}"
	mkdir -p "${pkgdir}${_destname2}"
	cp -r "${srcdir}/${_pkgname}/xfce4/"* "${pkgdir}${_destname2}"
}
