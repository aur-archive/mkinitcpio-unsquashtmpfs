# Maintainer: Gently <toddrpartridge@gmail.com>

pkgname=mkinitcpio-unsquashtmpfs
_pkgname=unsquashtmpfs
pkgver=0.86
pkgrel=1
pkgdesc="Hook that decompresses a squashfs image and mounts it to tmpfs."
arch=("any")
url="https://github.com/Gen2ly/mkinitcpio-unsquashtmpfs"
license=("GPL2")
depends=("")
changelog=
source=("git://github.com/Gen2ly/mkinitcpio-unsquashtmpfs")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir"/$pkgname
  git describe | sed 's/^v//;s/-.*//'
}

package() {
  cd "$srcdir/$pkgname"
  install -Dm644 hook        $pkgdir/usr/lib/initcpio/hooks/$_pkgname
  install -Dm644 install     $pkgdir/usr/lib/initcpio/install/$_pkgname
  install -Dm644 license.txt $pkgdir/usr/share/licenses/$pkgname/license.txt
}

# vim:set ts=2 sw=2 et:
