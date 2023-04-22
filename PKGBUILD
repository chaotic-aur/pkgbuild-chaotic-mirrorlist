# Maintainer: dr460nf1r3 <dr460nf1r3 at chaotic dot cx>
# Maintainer: Pedro H. Lara Campos <root@pedrohlc.com>
# Contributor: Florian Pritz <bluewind@xinu.at>
# Contributor: Dan McGee <dan@archlinux.org>

pkgname=chaotic-mirrorlist
pkgver=20230422
pkgrel=2
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

sha256sums=('0e32193cd55c76398fa885e804d4854f5b9970ffd9bd6dc278ba038b647e8c71')
