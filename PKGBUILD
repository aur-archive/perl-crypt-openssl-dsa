# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-crypt-openssl-dsa'
pkgver='0.14'
pkgrel='1'
pkgdesc="Digital Signature Algorithm using OpenSSL"
arch=('i686' 'x86_64')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('openssl>=1.0.1.e' 'perl')
makedepends=()
url='http://search.cpan.org/dist/Crypt-OpenSSL-DSA'
source=('http://search.cpan.org/CPAN/authors/id/T/TJ/TJMATHER/Crypt-OpenSSL-DSA-0.14.tar.gz')
md5sums=('61d06e8fe9c12e96743989ff13c7ea73')
sha512sums=('55bc9111a16e1c61572c6dc2da7e1ce6cf6de6736bf662d937268e514f2c7a1f9ee77228dac89cf3b6963c28727258756edf46f188c7b66f39f57140b04acbc6')
_distdir="Crypt-OpenSSL-DSA-0.14"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
