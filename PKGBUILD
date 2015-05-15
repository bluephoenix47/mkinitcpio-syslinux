pkgname=mkinitcpio-syslinux
pkgver=1.0
pkgrel=1
pkgdesc="Installs a mkinitcpio hook to automagically update syslinux after a new image is built."
url=""
license="MIT"
arch=('i686' 'x86_64')
depends=('syslinux')
source=(
"linux.preset"
"mkinitcpio.conf.syslinux"
"syslinux"
)
sha256sums=('0258e3113a2342c692969d9645b20c537fdc84e189d5707844e8f53c76ecadb4'
            'b61d4eff7635de7ee4de675e6d50dc36b5048645cbf52d32aacee3717f7c6338'
            'bbecfd29ba454593e427b4c5df38ccc82bcbf8a2817cd45b7ca59dde4db16292')
install=mkinitcpio-syslinux.install

package() {
  mkdir -p "$pkgdir/usr/lib/initcpio/install"
  install -D -o root -g root -m 644 \
    "$srcdir/syslinux" "$pkgdir/usr/lib/initcpio/install/"

  mkdir -p "$pkgdir/etc/mkinitcpio.d/"
  install -D -o root -g root -m 644 \
    "$srcdir/linux.preset" \
    "$pkgdir/etc/mkinitcpio-syslinux/etc/mkinitcpio.d/linux.preset"

  install -D -o root -g root -m 644 \
    "$srcdir/mkinitcpio.conf.syslinux" \
    "$pkgdir/etc/mkinitcpio.conf.syslinux"
}
