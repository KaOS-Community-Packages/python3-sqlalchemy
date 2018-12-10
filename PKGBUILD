pkgbase=python3-sqlalchemy
pkgname=('python3-sqlalchemy')
pkgver=1.2.14
pkgrel=1
arch=('x86_64')
url="http://www.sqlalchemy.org/"
license=('MIT')
makedepends=('python3-setuptools')
source=("https://pypi.io/packages/source/S/SQLAlchemy/SQLAlchemy-$pkgver.tar.gz")
sha512sums=('f6b89029180bc6f3e35bc17a1d80c111f6ce05f2f799bbdfee00c961e83aa2f95cbb363c85a5f97c18d5ff0aa1408c164621474cd6ddf8e63dd88da35de69539')

build() {
  cd "$srcdir"/SQLAlchemy-$pkgver
  python3 setup.py build
}

package_python3-sqlalchemy() {
  pkgdesc='Python SQL toolkit and Object Relational Mapper'
  depends=('python3')
  optdepends=('python3-psycopg2: connect to PostgreSQL database')

  cd SQLAlchemy-$pkgver
  python3 setup.py install --root="${pkgdir}"
  install -D -m644 LICENSE \
	  "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
