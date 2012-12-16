# Maintainer: Karol Babioch <karol@babioch.de>
# Contributor: allspark
pkgname=dropbear_initrd_encrypt
pkgver=0.10
pkgrel=1
pkgdesc="Allows for an encrypted root device to be unlocked remotely over SSH"
arch=('any')
url="https://mw.vc/2009/08/08/luks-pass-over-ssh-archlinux/"
license=('GPL')
depends=('dropbear' 'cryptsetup' 'mkinitcpio-nfs-utils' 'psmisc' 'iproute2')
install=$pkgname.install
source=('dropbear_hook' 'dropbear_install' 'encryptssh_hook' 'encryptssh_install')
md5sums=('1ffcec1d8e9227f65f79836626ffe453'
         '2404349a8949dc96792845b7e37a54a1'
         '39dd7d75248c3cb4ea624dc72a8b5459'
         '758df084cdacb9b43e3e7e322c7feaad')
backup=('usr/lib/initcpio/hooks/dropbear'
        'usr/lib/initcpio/hooks/encryptssh'
        'usr/lib/initcpio/install/dropbear'
        'usr/lib/initcpio/install/encryptssh')

build() {
  install -Dm644 "$srcdir/dropbear_hook"      "$pkgdir/usr/lib/initcpio/hooks/dropbear"
  install -Dm644 "$srcdir/dropbear_install"   "$pkgdir/usr/lib/initcpio/install/dropbear"
  install -Dm644 "$srcdir/encryptssh_hook"    "$pkgdir/usr/lib/initcpio/hooks/encryptssh"
  install -Dm644 "$srcdir/encryptssh_install" "$pkgdir/usr/lib/initcpio/install/encryptssh"
}
