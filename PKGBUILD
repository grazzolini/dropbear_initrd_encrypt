# Maintainer: Giancarlo Razzolini <grazzolini@gmail.com>
# Contributor: johnpatcher
# Contributor: chadversary
# Contributor: allspark
pkgname=dropbear_initrd_encrypt
pkgver=0.15
pkgrel=1
pkgdesc="Allows for an encrypted root device to be unlocked remotely over SSH"
arch=('any')
url="https://github.com/grazzolini/dropbear_initrd_encrypt.git"
license=('GPL3')
depends=('dropbear' 'cryptsetup' 'mkinitcpio-nfs-utils' 'psmisc' 'iproute2')
install=$pkgname.install
source=('ChangeLog' 'dropbear_hook' 'dropbear_install' 'encryptssh_hook' 'encryptssh_install' "$pkgname.install")
changelog='ChangeLog'
sha512sums=('8d69cf7a68cb2bd5d2e9172ab73fd8336fd598d32061235228b3fcc602b6a1dafa6fb62100935e60c4923b9f7891a4c6b4c39acf8fca363441320b808c2350dd'
            '6e024aeb28b78a19598b0062fbf42af2ac15f0bf234cc0c04f59a08e9c123df18c56b248c79cea4100594a67da4691cdcb7a2729805225728606da7747581ec7'
            'b15f389f064e716a5b801f807b2060c218a852ee8c2e0f70f2a40b40649ecbd35f964a43642934ebd20c51836918925c9ceef053e6011a7f3e3f2ec53ecffcb7'
            'f72d0bfaa03116af4a5f54226b1e63f73344eb8d078749e3a76408d0050660f3ba8ebd3df8f772a5e2d1f59bcc355d73cb04854e32b06a36248e446b67382592'
            '7e6820a3cafeb324e49c830cced3d8dc7adad727a6df15696cc09fd5ae69c2cbedcb3990fc9c6587b94ce042e183218b84664999694533f338a7205cd3688189'
            '190d624b6098661362ffdef13341030cb02c317135e742fa2e941939ed873f885f3deeb3361fad09163fec4dd580b06d57cc036df2391483bfab0a2076887cb2')

package() {
  install -Dm644 "$srcdir/dropbear_hook"      "$pkgdir/usr/lib/initcpio/hooks/dropbear"
  install -Dm644 "$srcdir/dropbear_install"   "$pkgdir/usr/lib/initcpio/install/dropbear"
  install -Dm644 "$srcdir/encryptssh_hook"    "$pkgdir/usr/lib/initcpio/hooks/encryptssh"
  install -Dm644 "$srcdir/encryptssh_install" "$pkgdir/usr/lib/initcpio/install/encryptssh"
}
