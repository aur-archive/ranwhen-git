# Maintainer: Haydania-Capri DiTori <me@capri.pw>

pkgname=ranwhen-git
pkgver=20140309
pkgrel=1
pkgdesc="Visualize when your system was running"
url="https://github.com/p-e-w/ranwhen"
arch=('any')
license=('GPLv3')
provides=('ranwhen')
depends=('python')
makedepends=('git')
source=()
md5sums=()

_gitroot="https://github.com/p-e-w/ranwhen.git"
_gitname="ranwhen"

build() {
	cd $srcdir

	msg "Connecting to github.com GIT server..."

	if [ -d ${srcdir}/$_gitname ] ; then
		cd $_gitname && git pull origin
		msg "The local files are updated."
	else 
		git clone $_gitroot
	fi
}

package() {
	cd "$srcdir/ranwhen"

	install -Dm755 "ranwhen.py" "$pkgdir/usr/bin/ranwhen"
}
