# Install Extra Toolchains for Amlogic Platform
Amlogic platform requires extra toolchains, follow the below steps to install these:

**Install Cross Compiler for U-Boot:**
```sh
$ sudo apt-get install gcc-arm-none-eabi
```
Note:
* We have verified that 'gcc-4.8.2 on Ubuntu 14.04' and 'gcc-4.9.3 on Ubuntu 16.04', both work fine on Vim platform, if you wanna try other gcc versions, may take a risk.


**Install Cross Compiler for Linux kernel:**
```sh
$ wget http://releases.linaro.org/14.09/components/toolchain/binaries/gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux.tar.bz2
$ sudo mkdir /opt/toolchains
$ sudo tar -xjf gcc-linaro-aarch64-linux-gnu-4.9-2014.09_linux.tar.bz2 -C /opt/toolchains
```
