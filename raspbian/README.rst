# raspbian that supports uberxmhf

## kernel build instructions
Build from source*:
  1. Download source `git clone https://github.com/raspberrypi/linux.git`
  2. `git checkout rpi-4.4.y`
  2. Use default config `make bcm2709_defconfig`
  3. `make zImage modules dtbs`
  4. `make modules_install`

     * Note for cross compiling, use `arb-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin` from https://github.com/raspberrypi/tools
       Modify `make` arguments to `make ARCH=arm CROSS_COMPILE=~/tools/arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/bin/arm-linux-gnueabihf-`

Using provided deb packages:     
  1. `dpkg -i linux-image-*`
  2. `dpkg -i linux-headers-*`
