# Maintainer: Atom Long <atom.long@outlook.com>

_pkgname=github-cli
pkgname=${_pkgname}-bin
pkgver=2.29.0
pkgrel=1
pkgdesc="The GitHub CLI"
arch=("i686" "x86_64")
url="https://github.com/cli/cli"
license=("MIT")
depends=("mailcap")
checkdepends=("openssh")
optdepends=("git: To interact with repositories"
            "org.freedesktop.secrets: Store credentials in system keyring")
provides=("github-cli=$pkgver")
conflicts=('github-cli')
source_x86_64=("${url}/releases/download/v${pkgver}/gh_${pkgver}_windows_amd64.zip")
source_i686=("${url}/releases/download/v${pkgver}/gh_${pkgver}_windows_386.zip")
sha256sums_x86_64=('031eb343ebff6f8cc712d58d79267ee00b0c61b37d6698927161daae895044c6')
sha256sums_i686=('3d626044e442e59c951ad8571cdf6bf07199c905fc0eb1de15283cde8fae9ae2')

package() {
	install -Dm755 bin/gh "$pkgdir/usr/bin/gh"
    install -Dm644 "LICENSE" "$pkgdir/usr/share/licenses/$_pkgname/LICENSE"
}
