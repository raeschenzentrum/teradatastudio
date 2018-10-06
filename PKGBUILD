pkgname=teradata-studio
pkgver=16.20.07.00
pkgrel=1
pkgdesc="TeradataStudio"
arch=('x86_64')
url="http://downloads.teradata.com/download/tools/teradata-studio"
license=('Proprietary')
depends=('java-runtime-headless-openjdk=8')
makedepends=('rpmextract')

source=("TeradataStudio64__linux_x86_64.${pkgver}-1.tar.gz"
        "TeradataStudio.desktop")
md5sums=('da71d9b6188403cbffa3a978b6376f82'
         '9b3b3b786508d44af4950889abbc0d87')

package() {
  install -dm755 ${pkgdir}/opt/teradata/TeradataStudio
  install -dm755 ${pkgdir}/usr/share/applications
  install -dm755 ${pkgdir}/usr/share/icons

  tar -xvaf ${srcdir}/*.tar.gz
  cd ${pkgdir}
  rpmextract.sh ${srcdir}/TeradataStudio*/*rpm

  install -m644 ${srcdir}/TeradataStudio.desktop ${pkgdir}/usr/share/applications/TeradataStudio.desktop
  ln -s /opt/teradata/TeradataStudio/icon.xpm ${pkgdir}/usr/share/icons/TeradataStudio.xpm
}
