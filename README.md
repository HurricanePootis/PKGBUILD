PKGBUILD


Fails to build (prev. did): Clementine-git

Fails to compile (prev. did): Gtkrawgallery

Fails to compile (never): Berry, Qscanner

Other:

* qstopmotion as been added in the AUR

***


**Tips for other packages**

Update source info

    makepkg --printsrcinfo > .SRCINFO

***

Extract .rpm .deb etc, avoid rpmextract

    bsdtar -xf $packagename.*

Package which use rpmextarct

* libstdc++296

***

for **fs-uae** Amiga emulator add CXXFlags in build()

	build() {
	cd $pkgname-$pkgver
	CXXFLAGS="${CXXFLAGS} -std=gnu++98"
