# Maintainer: everyx <lunt.luo#gmail.com>

pkgname=sing-geoip
pkgver=20231012
pkgrel=1

pkgdesc='sing-geoip database'
arch=('any')
_repo="SagerNet/${pkgname}"
url="https://github.com/${_repo}"
license=('GPL3')

optdepends=('sing-box: The universal proxy platform')

source=("${pkgver}.geoip-cn.db::${url}/releases/download/${pkgver}/geoip-cn.db"
        "${pkgver}.geoip.db::${url}/releases/download/${pkgver}/geoip.db"
        "${pkgver}.LICENSE::https://raw.githubusercontent.com/${_repo}/${pkgver}/LICENSE")
sha256sums=('ad3e6fa5c07f436420ed10ae41945e07b4176e29b894ce8258e98c1bfeb9b08a'
            '9475ed5d49acba8416c3d5b7aab9273019ef354b9532ca17aeb181faf2112316'
            '2f02b7486bcfa90d115c71a20437f3906b6fd5bef81c5dc0efd341399e89d0fd')

package() {
    install -Dm644 "${pkgver}.geoip-cn.db" "${pkgdir}/usr/share/${pkgname}/geoip-cn.db"
    install -Dm644 "${pkgver}.geoip.db"    "${pkgdir}/usr/share/${pkgname}/geoip.db"
    install -Dm644 "${pkgver}.LICENSE"     "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
