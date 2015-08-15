# Contributor: Olivier Esser ( Firstname.Lastname@gmail.com )

pkgname=blocklist-to-privoxy
pkgver=0.7
pkgrel=1
pkgdesc="Script which converts Opera urlfilter.ini into Privoxy (only tested with fanboy lists)"
arch=('any')
license=('MIT')
depends=("privoxy" "python2")
url=("http://freeshell.de/~oesser/scripts/blocklist-to-privoxy")
source=("http://freeshell.de/~oesser/scripts/blocklist-to-privoxy/blocklist-to-privoxy-${pkgver}"
        "http://freeshell.de/~oesser/scripts/blocklist-to-privoxy/tlds-alpha-by-domain.txt")
md5sums=("f66e955ddcdcc6ff9ef988cf23df251f"
         "970b60a8e17cbb8923eb0fe33983ac3a")

build() {
        cd ${srcdir}
	install -o root -g root -m 0755 -D ${srcdir}/${pkgname}-${pkgver} ${pkgdir}/usr/share/${pkgname}/${pkgname}-${pkgver}
        install -o root -g root -m 0644 -D ${srcdir}/tlds-alpha-by-domain.txt ${pkgdir}/usr/share/${pkgname}/tlds-alpha-by-domain.txt
        install -o root -g root -d  ${pkgdir}/usr/bin/
        ln -s ../share/${pkgname}/${pkgname}-${pkgver} ${pkgdir}/usr/bin/${pkgname}
} 
