# Download the Android Source Code 

**Tips:**
* All source code are released at: https://www.github.com/khadas
* Guidance for new starter: https://www.github.com/khadas/guide

**Steps:**
* Create a working directory for Android marshmallow:
```sh
$ mkdir -p ~/project/vim/mmallow
```
* Run `repo init` to bring down the Repo:
```sh
$ cd ~/project/vim/mmallow
$ repo init -u https://github.com/khadas/android_manifest.git
```

* Pull down the Android source tree:
```sh
$ repo sync -j4
```
The initial sync operation will take an hour or more to complete. 

When complete the sync operation, the Android source files will be located in your working directory under their project names:
```
$ ls
abi       common       device        hardware         out               sdk
art       cts          docs          libcore          packages          system
bionic    dalvik       external      libnativehelper  pdk               tools
bootable  developers   fbc3-release  Makefile         platform_testing  uboot
build     development  frameworks    ndk              prebuilts         vendor
$
```
When everything is done, recommended to create your own branch:
```sh
$ repo start Vim --all
```

**See also:**
* [Android official documents](https://source.android.com/source/downloading.html)
* [Build Android Source Code](https://github.com/khadas/documents/blob/master/BuildingAndroid.md)
