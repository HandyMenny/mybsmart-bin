# Maintainer: HandyMenny <handymenny[at]outlook[dot]com>
pkgname=my-bsmart-bin
s_pkgname=MybSmart
pkgver=1.7.2
pkgrel=1
pkgdesc="MybSmart desktop application"
arch=('i686' 'x86_64')
if [ "${CARCH}" = "x86_64" ]; then
  sha256sums=(SKIP)
  _carch=x64
elif [ "${CARCH}" = "i686" ]; then
  sha256sums=('c6e56eaab1ab4b1d690ee2c6ff18ac3d1773f59e7b243bfedd81ac5fd0f42fcf')
  _carch=ia32
fi
license=('custom:"Copyright: Applix Education <webmaster@bsmart.it"')
url="http://www.bsmart.it"
source=("http://res.bsmart.it.s3.amazonaws.com/mybsmart_desktop/releases/production/linux/$_carch/$s_pkgname.deb")
depends=('gconf' 'libcap' 'gtk2' 'udev' 'libgcrypt' 'libnotify' 'libxtst' 'nss' 'python' 'xdg-utils')

package() {
	tar -Jxf data.tar.xz -C "${pkgdir}"	
	chmod -R 755 ${pkgdir}/usr/{,share/{,applications}}
	chmod -R 755 ${pkgdir}/opt/
}
