#
# Bamboo - A Vietnamese Input method editor
# Copyright (C) 2018-2020 Luong Thanh Lam <ltlam93@gmail.com>
# Copyright (C) 2021 Nguyen Tran Hoang <tranhoangcore@gmail.com>

# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.


pkgname=ibus-bamboo
pkgver=0.6.7
pkgrel=1
[[ $pkgrel -eq 1 ]] && _pkgver=$pkgver || _pkgver="$pkgver-$((pkgrel-1))"
pkgdesc='A Vietnamese IME for IBus'
arch=(any)
license=(GPL3)
url="https://github.com/BambooEngine/ibus-bamboo"
depends=('ibus')
makedepends=('go' 'libx11' 'libxtst')
source=("$pkgname-$_pkgver.tar.gz"::"https://github.com/BambooEngine/$pkgname/archive/v$_pkgver.tar.gz")
sha256sums=('92d49fe232f241b3e62348c49883aed8a439f256bf6c39034270e069e6c34563')
options=('!strip')
conflicts=(ibus-bamboo-git)

build() {
  cd "$pkgname-$_pkgver"

  make
}


package() {
  cd "$pkgname-$_pkgver"

  make DESTDIR="$pkgdir/" install
}
