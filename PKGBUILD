# Maintainer: Serhii Hordiienko <phrippy2@gmail.com>

pkgname=update-hosts
pkgver=20251226
pkgrel=3
pkgdesc="Systemd timer and script that refreshes the system hosts file"
arch=('any')
url="https://github.com/phrippy/update-hosts"
license=('custom')
depends=('curl' 'systemd')
source=('update_hosts'
        'update-hosts.service'
        'update-hosts.timer')
sha256sums=('e0b7774d2a95e54a91af0911806d256334d88621194aedd95d545018653a6f99'
            '34665c6840e01e6d01e11d4a46fb77612e76a65788eb9bb7b8cfcaef29a2ea30'
            '740afa1de50dec1332ebbb4317c47f22e435b0e539ccde131cb90bd2df3eaacd')

package() {
    install -Dm755 "${srcdir}/update_hosts" "${pkgdir}/usr/bin/update_hosts"
    install -Dm644 "${srcdir}/update-hosts.service" "${pkgdir}/usr/lib/systemd/system/update-hosts.service"
    install -Dm644 "${srcdir}/update-hosts.timer" "${pkgdir}/usr/lib/systemd/system/update-hosts.timer"
}
