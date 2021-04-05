# Maintainer: Deadgar <deadgar@protonmail.com>
_basename=mullvad
pkgname=${_basename}-runit
pkgver=20210405
pkgrel=1
pkgdesc="Runit service for Mullvad Desktop App"
arch=('any')
url="https://github.com/D3adgar/mullvad-runit"
license=('GPL-2.0-or-later')
conflicts=()
source=("${_basename}.run")
sha256sums=('726e1d33be434b702a656de65e66b6c9f283e1afe0e660cb67414b87e8b04ce1')

package() {
  for x in run ; do
    install -Dm755 "$srcdir/${_basename}.${x}" "$pkgdir/etc/runit/sv/${_basename}/${x}"
  done
}
