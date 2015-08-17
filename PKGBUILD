# Author: Pierre-Olivier Vauboin <povauboin@gmail.com>

pkgname=onesixtyone
pkgver=0.7
pkgrel=1
pkgdesc='An SNMP scanner that sends multiple SNMP requests to multiple IP addresses'
arch=('i686' 'x86_64')
url="http://labs.portcullis.co.uk/application/onesixtyone/"
license=('GPL')
depends=('glibc')
source=("http://labs.portcullis.co.uk/download/onesixtyone-${pkgver}.tar.gz")
sha1sums=('FD4CB35151D57DF1EF357F4CA8F69A99D85862B0')

build() {
    cd ${pkgname}-${pkgver}
    make
}

package() {
    cd ${pkgname}-${pkgver}
    mkdir -p ${pkgdir}/usr/bin
    mkdir -p ${pkgdir}/usr/share/onesixtyone
    make BINDIR=${pkgdir}/usr/bin/ install
    install -m 0644 dict.txt ${pkgdir}/usr/share/onesixtyone/
}
