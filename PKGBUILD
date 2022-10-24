# Maintainer: Leonidas P. <jpegxguy at outlook dot com>
# Maintainer: Jerry <isjerryxiao at outlook dot com>
# Contributor: Anes Belfodil <ans.belfodil at gmail dot com>
# Contributor: David Rheinsberg <david.rheinsberg at gmail dot com>
# Contributor: David Herrmann <dh.herrmann at gmail dot com>
# Contributor: Ian P. Cooke <ipc at informatic dot io>

_pkgname=qemu-user-static
_pkgver="7.1"
_pkgadditver="+dfsg-2+b1"
pkgname=${_pkgname}-bin
pkgver=${_pkgver//\~/}
pkgrel=7
pkgdesc='A generic and open source machine emulator, statically linked'
arch=('x86_64' 'i686' 'aarch64' 'armv7h' 'armv6h')
url="http://wiki.qemu.org"
license=('GPL2' 'LGPL2.1')
depends=('binfmt-qemu-static')
provides=("qemu-user" "${_pkgname}" "qemu-arm-static")
conflicts=("qemu-user" "${_pkgname}" "qemu-arm-static")

source_x86_64=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_amd64.deb")
source_i686=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_i386.deb")
source_aarch64=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_arm64.deb")
source_armv7h=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_armhf.deb")
source_armv6h=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_armel.deb")

sha256sums_x86_64=("180a9275c6d11c292ce0b36f7927bbca6ed836fabb8c6fc2d6ccd9e5ce3b235e")
sha256sums_i686=("f79522069126c4dd6babbdf489b9b18bd9357c18439f10a86edced4d33c1fa42")
sha256sums_aarch64=("74eaa4491799502c89e75218dbbc89c416b7d5320ae56fbec2129727e50541d1")
sha256sums_armv7h=("b1c1249dec6f7470cf20ee4be7c60e0c94f87b48e6ddbe5dc70761d5417b6fbe")
sha256sums_armv6h=("0900c823086e85e07cafdaebc0bdf9a4c2ab03d98503be373e7982aabd7a9284")

package() {
	tar -C "${pkgdir}" -xf "${srcdir}/data.tar.xz" --exclude=./usr/share/man/man1/qemu-debootstrap.1.gz ./usr/bin ./usr/share/man
}
