**Status**

* Neobarok: on AUR
* openage-git: on AUR (adopted)
* qstopmotion: on AUR (not me)

From AUR3: 

| Name       | status            |
| ---------- | --------------- |
| qcomicbook | updated version |
| spe        | plain aur3 import |
| squeezeplay | plain aur3 import |

From AUR: 

| Name        | status                               |
| ----------- | ---------------------------------- |
| moksha-modules-extra-git | build fix |
| openage-git | install fix (adopted)                       |
| upplay-qt5      | updated compiling flag to build in QT5 |
| upplay-qt5-git  | updated compiling flag to build in QT5 |
| dvdae-bin   | updpkgsums                         |
| solar2      | updpkgsums                         |
| voltra      | updpkgsums                         |

Reworked from AUR or Arch:

| Name                     | modified to                    |
| ------------------------ | ----------------------- |
| clementine-light-git     | disable plugins        |
| clementine-light-qt5-git | disable plugins        |
| mpv-vaapi | enabled vaapi |
| phoronix-test-suite-milestone   | build milestone version |
| roonbridge | add 'armv7h' & 'aarch64' architectures |
| smbnetfs | enable gnome keyring |
| smbnetfs-git | build git version with gnome keyring enabled |
| twin-git | build git version |
| xf86-video-sisimedia-rkrell-git | video driver for SiS 671/771 cards |

Original:

| Name                  | Description                                     |
| --------------------- | --------------------------------------- |
| madrigal-git          | Qt5 OpenHome Control Point, in development               |
| maxmonitoring         | Monitoring tool for Solarmax inverters    |
| neobarok              | 3D modeling software                     |
| openboard-bin         | Openboard Ubuntu binary version          |
| qiviever              | QT image viewer                          |
| qmultirecord          | Simultaneously burn multiple ISO files on several optical drives |
| quickhash-gui-bin     | Graphical hashing utility, Debian binary version |
| sacd-decoder          | Command line SACD decoder                |

***

Others pkgbuilds are experimental, work in progress or fails:

| Name                     |                     |
| ------------------------ | ----------------------- |
| squeezeplay | Git versions don't compile |
| gravit-designer | In progress |


**Tips for other packages**

Update source info

    makepkg --printsrcinfo > .SRCINFO

***

Extract .rpm .deb, avoid rpmextract, debtap, etc..

    bsdtar -xf $packagename.*

***

Package which use rpmextarct

* libstdc++296

***

for **fs-uae** Amiga emulator add CXXFlags in build()

	build() {
	cd $pkgname-$pkgver
	XXFLAGS="${CXXFLAGS} -std=gnu++98"
	./configure --prefix=/usr
	make 
	}
