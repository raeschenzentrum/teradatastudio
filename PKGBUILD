pkgname=teradata-studio
pkgver=16.20.00.01
pkgrel=1
pkgdesc="TeradataStudio"
arch=('x86_64')
url="http://downloads.teradata.com/download/tools/teradata-studio"
license=('Proprietary')
depends=('java-runtime-headless-openjdk=8')
makedepends=('unzip')

source=("TeradataStudio64__linux_x86_64.${pkgver}-1.tar.gz"
        "TeradataStudio.desktop")
md5sums=('1a913bba69be5104c34e98ef3216c834'
         '9b3b3b786508d44af4950889abbc0d87')

package() {
  install -dm755 ${pkgdir}/opt/teradata/TeradataStudio
  install -dm755 ${pkgdir}/usr/share/applications
  install -dm755 ${pkgdir}/usr/share/icons

  tar -xvaf ${srcdir}/*.tar.gz
  unzip -q -o ${srcdir}/TeradataStudio64.${pkgver}/TeradataStudio-linux.gtk.x86_64.zip -d ${pkgdir}/opt/teradata/TeradataStudio

  install -m644 ${srcdir}/TeradataStudio.desktop ${pkgdir}/usr/share/applications/TeradataStudio.desktop
  ln -s /opt/teradata/TeradataStudio/icon.xpm ${pkgdir}/usr/share/icons/TeradataStudio.xpm
}
