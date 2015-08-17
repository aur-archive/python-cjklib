# Maintainer: Alexey Zinovyev <root@x3al.pp.ru>

pkgname=python-cjklib
pkgver=0.3
pkgrel=3
pkgdesc="Han character library for CJKV languages"
arch=('any')
url="http://code.google.com/p/cjklib/"
license=('LGPL')
depends=('python2-sqlalchemy' 'sqlite3' 'python2')
options=(!emptydirs)
source=("http://cjklib.googlecode.com/files/cjklib-$pkgver.tar.gz")
md5sums=('e5ea0997fbe0a4398f3693ba3252ebfd')


build() {
  cd "$srcdir/cjklib-$pkgver"
  python2 setup.py install --root="$pkgdir" --optimize=1 
  find "$pkgdir" -name '*.py' -print0|xargs -0 \
	   sed -i -e 's,^#!/usr/bin/env python$,#!/usr/bin/env python2,' \
	   -e 's,^#!/usr/bin/python$,#!/usr/bin/python2,'

}
