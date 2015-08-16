# Contributor: twa022 <twa022 at gmail dot com> 
# Maintainer: H.Gökhan Sarı <me at th0th dot me>

pkgname=gtk-theme-hope
pkgver=20120317
pkgrel=3
pkgdesc="Matching GTK2, GTK3, Gnome-shell, & XFCE Hope Themes"
url="http://grvrulz.deviantart.com/art/Hope-gtk3-206207315"
license=('cc-by-nc-sa-3.0')
arch=('any')
depends=('gtk-engine-murrine')
optdepends=('gtk-engine-unico: for the gtk3 theme'
            'xfwm4: for XFCE theme'
            'openbox: for Openbox theme'
            'gnome-shell: for Gnome Shell theme'
            'ttf-pt-sans: Recommended Fonts')
[ "$CARCH" == "x86_64" ] && optdepends+=('lib32-gtk-engine-murrine: 32 bit application GTK2 theme support')
source=("${pkgname}-${pkgver}.7z::http://fc09.deviantart.net/fs71/f/2012/077/9/b/hope_gtk3_by_grvrulz-d3erqkz.7z"
        'whitefontsfix.patch')

package() {
  cd ${srcdir}
  patch -p0 < "${srcdir}"/whitefontsfix.patch
  mkdir -p ${pkgdir}/usr/share/themes/
  cp -r ${srcdir}/Hope ${pkgdir}/usr/share/themes/
  cp -r ${srcdir}/Hope-DT ${pkgdir}/usr/share/themes/
  find "${pkgdir}" -name *~ -exec rm '{}' \;
}

sha256sums=('1d2f526ffb74597de37de4ff22a60c4996cd9c8ad82d26dc3bfb674407ac9cd6'
            'eff57c5458eb6b7495bab74707c237337ffb2b26dd6ec6d2b1253454bd52c919')
