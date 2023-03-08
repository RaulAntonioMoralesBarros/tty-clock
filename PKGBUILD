# Maintainer: Kyle Keen <keenerd@gmail.com>
# Contributor: Daniel J Griffiths <ghost1227@archlinux.us>

pkgname=tty-clock
pkgver=2.3
pkgrel=1
pkgdesc="Digital clock in ncurses"
arch=('i686' 'x86_64')
url="http://github.com/xorg62/tty-clock"
license=('unknown')
depends=('ncurses')
source=("$pkgname-$pkgver.tgz::https://github.com/xorg62/tty-clock/archive/v$pkgver.tar.gz")

md5sums=('2452b5a3286d4d7993913cbfc744ed1e')

#patched bug - DATE:05/03/2023
codelinebug='mvwprintw(ttyclock->datewin, (DATEWINH / 2), 1, ttyclock->date.datestr);'
codelinepatch='mvwprintw(ttyclock->datewin, (DATEWINH / 2), 1,"%s" ,ttyclock->date.datestr);'

build() {
  cd "$srcdir/$pkgname-$pkgver"
  sed -i 's/mvwprintw(ttyclock->datewin, (DATEWINH \/ 2), 1, ttyclock->date.datestr);/mvwprintw(ttyclock->datewin, (DATEWINH \/ 2), 1, "%s",ttyclock->date.datestr);/g' "ttyclock.c"
  read -rsp $'Press enter to continue...\n'  
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -Dm755 $pkgname "$pkgdir/usr/bin/$pkgname"
  install -Dm655 tty-clock.1 "$pkgdir/usr/share/man/man1/tty-clock.1"
} 
