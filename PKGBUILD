# Maintainer: dr460nf1r3 <dr460nf1r3 at chaotic dot cx>
# Maintainer: Pedro H. Lara Campos <root@pedrohlc.com>
# Contributor: Florian Pritz <bluewind@xinu.at>
# Contributor: Dan McGee <dan@archlinux.org>

pkgname=chaotic-mirrorlist
pkgver=20220418
pkgrel=1
pkgdesc="Chaotic-AUR mirrorlist to use with Pacman"
arch=('any')
url="https://aur.chaotic.cx"
license=('GPL')
backup=(etc/pacman.d/chaotic-mirrorlist)
source=(mirrorlist)

# NOTE on building this package:
# * Go to the trunk/ directory
# * Run bash -c ". PKGBUILD; updatelist"
# * Update the checksums, update pkgver
# * Build the package

updatelist() {
  rm -f mirrorlist
  curl -o mirrorlist "$url/mirrorlist.txt"
}

package() {
  mkdir -p "$pkgdir/etc/pacman.d"
  install -m644 "$srcdir/mirrorlist" "$pkgdir/etc/pacman.d/chaotic-mirrorlist"
}

sha256sums=('dad7a4364e4c9d0eef5a339fe0fa7fe4c13b38fc42dbf8e70d7b2bfc5559a9e5')
