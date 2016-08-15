pkgname=arc-themes
commit=5cf4407-ee42419 #=light-dark
pkgver=16.08.11
pkgrel=1
pkgdesc='Arc customization for Plasma 5'
arch=('x86_64')
url='https://github.com/varlesh/Arc-KDE'
license=('CCPL:by-sa')
options=('!strip')
makedepends=('make' 'git')
depends=('imagemagick')
optdepends=("gtk-theme-arc: A flat theme with transparent elements for GTK 3, GTK 2 and Gnome-Shell"
            "papirus-icon-theme-kde: Papirus icon theme for KDE"
            "yakuake: A drop-down terminal emulator based on KDE konsole technology"
            "konsole: Terminal")
source=("arc-light::git+https://github.com/varlesh/Arc-KDE.git#commit=${commit/-*/}"
        "arc-dark::git+https://github.com/varlesh/Arc-Dark-KDE.git#commit=${commit/*-/}")
sha256sums=('SKIP'
            'SKIP')

package() {
    make -C "arc-light" install DESTDIR="$pkgdir"
    make -C "arc-dark" install DESTDIR="$pkgdir"
}
