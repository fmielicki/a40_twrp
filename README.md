# a40_twrp
TWRP Device tree for SM-A405FN

# Disclaimer
Use, build, modify at your own risk. I'm not responsible for anything you do to your device.

IMPORTANT! AT THE CURRENT STATE, THIS WILL RENDER YOUR DEVICE UNBOOTABLE! MAKE SURE YOU KNOW WHAT YOU ARE DOING BEFORE ATTEMPTING TO COMPILE AND FLASH THIS! It is possible to get back into the download mode to flash a stock recovery, but it is NOT an easy thing to do.

## Sources
I have modified some files from this great repository: https://github.com/geiti94/android_device_samsung_a30dd

## Prerequisites
You will need a patched vbmeta.img. Do this with Magisk Manager.
You will need a compile environment for TWRP images.

## Build
To build, clone the repository to devices/samsung/a40

``source build/envsetup.sh``
``lunch "omni_a40"-eng``
``make clean``
``make -j* recoveryimage``

Replace * with your CPU thread count. For me it would be ``make -j12 recoveryimage`` since I build on Ryzen 5 1600.
