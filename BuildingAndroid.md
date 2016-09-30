# Building Android Source Code


**Preperations:**
* [Establishing a Build Environment](http://source.android.com/source/initializing.html)
* [Downloading the Android Source](https://github.com/khadas/documents/blob/master/DownloadAndroidSourceCode.md)
* [Install toolchains for Amlogic platform](https://github.com/khadas/documents/blob/master/InstallToolchainsForAmlogicPlatform.md)


**Build U-Boot:**
```sh
$ cd ~/project/vim/mmallow/uboot
$ make CROSS_COMPILE=aarch64-linux-gnu- kvim_defconfig
$ make CROSS_COMPILE=aarch64-linux-gnu-
```
Gernerated images:
* fip/u-boot.bin: for onboard EMMC storage booting
* fip/u-boot.bin.sd.bin: for external TF card booting


**Build Android:**
```sh
$ source build/envsetup.sh
$ lunch kvim-user-32
$ make -jN otapackage
```
Notice:
* Replace 'N' as the number you want when you run 'make -jN'
* Use 'userdebug' instead if build android with debug mode:
	```
	$ lunch kvim-userdebug-32
	```

Gernerated images:
* out/target/product/kvim/update.img


**Build Linux kernel:**

If you wanna build linux kernel separately, run:
```sh
$ source device/khadas/kvim/mkern.sh
```


**See also:**
