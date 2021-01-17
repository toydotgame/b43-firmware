# Maintainer: Xavion <Xavion (dot) 0 (at) Gmail (dot) com>
# Forked by: Toydotgam <toydotgame (at) gmail (dot) com>
#	I changed it so that the entire package can be cloned and built locally, in case the AUR package gets 404'd one day.

pkgname=b43-firmware
pkgver=6.30.163.46
pkgrel=1
pkgdesc="Firmware for Broadcom B43 wireless networking chips - latest release"
arch=("any")
url="https://wireless.wiki.kernel.org/en/users/Drivers/b43"
license=("unknown")
depends=("linux>=3.2")
makedepends=("b43-fwcutter>=018")
conflicts=(b43-firmware-classic)
install=${pkgname}.install
options=(!emptydirs)
source=(./src/broadcom-wl-6.30.163.46.tar.bz2)

package() {
	cd "${srcdir}"

	# Directories
	install -d "${pkgdir}"/usr/lib/firmware/

	# Application
	b43-fwcutter -w "${pkgdir}"/usr/lib/firmware/ broadcom-wl-${pkgver}.wl_apsta.o

	# Messages
	#msg "You should add 'b43' to the 'MODULES' array of your '/etc/rc.conf' file."
}

sha1sums=('237d29a7701429054f5c82c000ef2d9aa6f2c3db')
