# Contributor: joshua d <josh@kurotek.com>
# maintainer: joshua d <josh@kurotek.com>
# category: office

pkgname=toggl-desktop-beta
pkgver=4.0.0
pkgrel=1
pkgdesc="Time tracker application"
arch=('i686' 'x86_64')
url="http://www.toggl.com/"
license=("Closed source")
groups=()
depends=('qt>=4.6.0 libpng12')
provides=()
conflicts=('toggl')
replaces=('toggl')
backup=()
options=()
if [ "$CARCH" == 'x86_64' ]
then
  source=( https://download.toggl.com/toggldesktop/edge/toggl-desktop_amd64.deb TogglDesktop.desktop)
  md5sums=(ff27d799cf19e679a2b683e284102678 93080f4318809706439c7f9efc44f43a)
else
  source=(https://download.toggl.com/toggldesktop/edge/toggl-desktop_i386.deb TogglDesktop.desktop)
  md5sums=(ff27d799cf19e679a2b683e284102678 93080f4318809706439c7f9efc44f43a)
fi
noextract=()
#generated with 'makepkg -g'

build() {
  cd "$srcdir/"

  #extract archive
  if [ "$CARCH" == 'x86_64' ]
  then
   ar p toggl-desktop_amd64.deb data.tar.gz | tar xz
  else
   ar p toggl-desktop_i386.deb data.tar.gz | tar xz
  fi

  # Manual install
  mkdir -p $pkgdir/usr
  cp -a usr/* $pkgdir/usr
  cp TogglDesktop.desktop $pkgdir/usr/share/applications/
  
  mkdir -p $pkgdir/opt
  cp -a opt/* $pkgdir/opt
}

# vim:set ts=2 sw=2 et:
