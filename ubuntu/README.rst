# ubuntu distributions that support uberxmhf

## kernel build instructions

Build from source:
  1. Download source `git clone git://kernel.ubuntu.com/ubuntu/ubuntu-<version>.git`
  2. Copy `.config` for kernel version into source directory
  3. `make`
  4. `make modules_install`
  5. `fakeroot make install`
  6. reboot

Using provided deb packages:
  1. `dpkg -i linux-image-*`
  2. `dpkg -i linux-headers-*`
  3. reboot
