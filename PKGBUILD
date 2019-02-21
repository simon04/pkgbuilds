# Maintainer: Lorenzo Fontana <lo@linux.com>
pkgname=coredns-bin
pkgver=1.3.1
pkgrel=1
pkgdesc="CoreDNS is a DNS server that chains plugins (official binary version)"
arch=('x86_64')
conflicts=('coredns')
url="https://github.com/coredns/coredns"
license=('Apache')
provides=('coredns')
source=(coredns_x64_${pkgver}.tar.gz::https://github.com/coredns/coredns/releases/download/v${pkgver}/coredns_${pkgver}_linux_amd64.tgz
coredns.service
coredns-sysusers.conf)

sha256sums=('1e88337650de8c878ab30a0d06adbf83c46c1cbea0d7d98f7f40c0346c39eed6'
'030cd8e938c293c11a9acdb09b138f98b37874772072336792ec4bf0d9eff9b1'
'536d03f8b20b0d2d6e8f96edd7e4e4dd7f6fef39ab0e952522d8725f3cc186b7')

package() {
    install -Dm755 "$srcdir/coredns" "$pkgdir/usr/bin/coredns"
    install -Dm644 "$srcdir/coredns.service" "$pkgdir/usr/lib/systemd/system/coredns.service"
    install -Dm644 "$srcdir/coredns-sysusers.conf" "$pkgdir/usr/lib/sysusers.d/coredns.conf"
    install -d "${pkgdir}/etc/coredns"
}
