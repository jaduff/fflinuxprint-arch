pkgname=fflinuxprint
pkgver=1.1.4_3
pkgdesc='An Arch repackage of the FujiFilm cups printer drivers'
pkgrel=1
arch=('x86_64')
url='https://support-fb.fujifilm.com/processDriverForm.do?ctry_code=AU&lang_code=en&d_lang=en&corp_pid=AP6C5571&rts=null&model=ApeosPort-VI+C5571&type_id=2&oslist=Linux+64+bit&lang_list=en'
license=('GPL-2.0-or-later')
_packagename='fflinuxprint_1.1.4-3_amd64'
_filename=${_packagename}.zip
source=("https://support-fb.fujifilm.com/driver_downloads/$_filename")
sha256sums=('fed58d5289b15690dcfdca096ceb4ccc73ad638f1ee1844c8f88fce8e6251d67')
depends=(cups)


package() {
        cd "${srcdir}"
        cd $_packagename
        echo "unpacking deb"
        ar -x ${_packagename}.deb
        tar -xf data.tar.xz
	mkdir "${pkgdir}"/usr
        cp -R ./usr/share "${pkgdir}/usr/share"
}
