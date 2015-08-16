# $Id: PKGBUILD 59239 2011-11-21 15:32:18Z spupykin $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Sergej Pupykin <pupykin.s+arch@gmail.com>

pkgname=jabwebhist
pkgver=200801
pkgrel=3
pkgdesc="jabber message history (XEP-0136) browser"
arch=('any')
url="http://bepointbe.be/jabwebhist/"
license=('GPL')
depends=(php)
#source=(http://bepointbe.be/files/jabwebhist-$pkgver.tar.gz)
source=(http://arch.p5n.pp.ru/~sergej/dl/2011/jabwebhist-$pkgver.tar.gz)
md5sums=('488737c58b4f1b5d5f34f5883a7571b7')

build() {
  cd $srcdir/jabwebhist

  patch -p1 index.php <<EOF
diff -r jabwebhist.org/index.php jabwebhist/index.php
35c35
< <?
---
> <?php
EOF

  patch -p1 prefs.php <<EOF
diff -r jabwebhist.org/prefs.php jabwebhist/prefs.php
35c35
< <?
---
> <?php
EOF

  install -d -m0755 $pkgdir/srv/http/jabwebhist
  cp *.php $pkgdir/srv/http/jabwebhist
}
