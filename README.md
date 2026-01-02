# postmarketOS_xiaomi_earth
PostmarketOS on Xiaomi Redmi 12C Aether/Earth

#How to build
pmbootstrap init

pmbootstrap build linux-xiaomi-earth --force
pmbootstrap build firmware-xiaomi-earth --force
pmbootstrap build device-xiaomi-earth --force

pmbootstrap install

pmbootstrap flasher --method=fastboot export

*.img files in chroot_native/home/pmos/ directory 

#How to flash

#with pmbootstrap
adb reboot bootloader

pmbootstrap flasher --method=fastboot flash_kernel
pmbootstrap flasher --method=fastboot flash_rootfs

#with fastboot

adb reboot bootloader

fastboot flash boot /path/to/boot.img
fastboot flash system /path/to/system.img