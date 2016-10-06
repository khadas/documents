# Download the Android Source Code


## Overview
* All source code are released at: https://www.github.com/khadas
* Guidance for new starter: https://www.github.com/khadas/guide


## Steps to download Android source code
* **Create an empty directory to hold your working files:**
```sh
$ mkdir -p ~/project/vim/mmallow
$ cd ~/project/vim/mmallow
```

* **Run `repo init` to bring down the repositories:**
```sh
$ repo init -u https://github.com/khadas/android_manifest.git
```

* **Run `repo sync` to pull down the Android source tree:**
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

*Tips: you might need to run above command repeatly if it failed halfway. Or you can try with below script instead:*
```sh
#!/bin/bash
repo sync -j4
while [ $? = 1 ]; do
	echo "Sync failed, repeat again:"
	repo sync -j4
done
```

* **Create a new branch for development:**
```sh
$ repo start Vim --all
```


## Further Reading
* [Android official documents](https://source.android.com/source/downloading.html)
* [Build Android Source Code](https://github.com/khadas/documents/blob/master/BuildingAndroid.md)
