# Maintainer: Simon Cruanes <simon.cruanes.2007@m4x.org>
pkgname=kodkodi
pkgver=2.0
pkgrel=1
epoch=
pkgdesc="kodkodi, a CLI interface to the constraint solver Kodkod"
arch=('any')
url="http://alloy.mit.edu/kodkod/index.html"
license=('MIT')
groups=()
depends=(
  'glibc'
  'lib32-glibc'
  'java-environment-common'
  'jre7-openjdk-headless'
  'gcc-libs-multilib'
  )
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://cedeela.fr/~simon/files/kodkodi-all.tar.gz")
noextract=()
md5sums=("6a32bacd3bde44fa6fdfd8a14226e5a0")
validpgpkeys=()

LICENSE='''The MIT License (MIT)

Copyright (c) <year> <copyright holders>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
'''

prepare() {
  echo "$LICENSE" > LICENSE
}

#build() { }

TO_COPY=('kodkodi' 'jar-kodkodi' 'jni-kodkodi')

check() {
  for i in ${TO_COPY[*]} ; do
    ls "$i" || exit 1 > /dev/null;
  done
}

package() {
  mkdir -p "$pkgdir/usr/bin/"
  cp -r ${TO_COPY[*]} "$pkgdir/usr/bin/"
  install -D -m 644 LICENSE "$pkgdir/usr/share/licenses/${pkgname}/LICENSE"
}
