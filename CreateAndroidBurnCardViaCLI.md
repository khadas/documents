# Create Android Burning Card Via Command Line


## Preperations:
* Build to get or [download](https://github.com/khadas/documents/blob/master/FirmwareResources.md) the latest U-Boot file for SD card.
* You might need to [format the TF Card Via fdisk](https://github.com/khadas/documents/blob/master/FormatTFCardViaFdisk.md) if your card exists more than one partitions.


## Create the Burning TF Card
**Pop the TF card into your PC, and make sure the disk is unmounted:**
```sh
$ umount /dev/sdb1
```

**Format the TF Card as Fat32:**
```sh
$ sudo mkfs.vfat /dev/sdb1 
```

**Use `dd` to write the bootloader/u-boot to the first sector of TF Card:**
```sh
$ sudo dd if=u-boot.bin.sd.bin of=/dev/sdb bs=1 count=444 && sync 
$ sudo dd if=u-boot.bin.sd.bin of=/dev/sdb bs=512 skip=1 seek=1 && sync 
```
*Notice: u-boot file `u-boot.bin.sd.bin` is build for SD, and `u-boot.bin` is for EMMC.*

**Copy the images to TF Card:**

Pop the TF card in again, then run the following command:
```sh
$ cp -a aml_sdc_burn.ini Vim_Marshmallow_160928/update.img /media/gouwa/9CE9-3938/
```
*Tips: `aml_sdc_burn.ini` is a configuration file for u-boot to burn/download images into onboard EMMC storage*

**Eject the TF Card:**
```sh
$ sudo eject /dev/sdb
```

Done!


## Further Reading:
* [Create OpenELEC_Booting_Card Via CLI](https://github.com/khadas/documents/blob/master/CreateOpenELECBootingCardViaCLI.md)
* [Booting_Card Vs Burning Card](https://github.com/khadas/documents/blob/master/BootingCardVsBurningCard.md)
