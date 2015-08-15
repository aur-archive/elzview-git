# Maintainer: Maximilien Noal (noal dot maximilien at gmail dot com) [AUR: xcomcmdr]

pkgname=elzview-git
_gitname=touhy
_pkgprog=elzview
pkgver=69.c2e9fda
pkgrel=1
pkgdesc="Elzen's picture-viewer and quickviewer"
arch='any'
license='GPL3'
url='http://fadrienn.irlnc.org/touhy/'
groups='touhy'
depends=('touhy-git' 'pygtk')
optdepends=('pywebkitgtk: SVG support'
  'python2-imaging: display pixel size of image files')
makedepends='git'
md5sums=('SKIP')
source=('git://fadrienn.irlnc.org/touhy')

pkgver() {
  cd ${srcdir}/${_gitname}
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd ${srcdir}/${_gitname}
  mkdir -p ${pkgdir}/usr/bin
  install ${_pkgprog} ${pkgdir}/usr/bin
  install -Dm 644 resources/appinfos/${_pkgprog}.desktop \
    ${pkgdir}/usr/share/applications/${_pkgprog}.desktop
}
