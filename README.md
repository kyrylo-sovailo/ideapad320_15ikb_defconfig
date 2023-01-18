# Lenovo Ideapad 320-15IKB

Kernel configuration for [Lenovo Ideapad 320-15IKB \(Type 80XL\) laptop](pcsupport.lenovo.com/us/en/products/laptops-and-netbooks/300-series/320-15ikb/)

This is a built-in configuration capable of running an average laptop with almost all functionality enabled. Bluetooth, HDMI, MiniJack are not implemented / not tested. The kernel is `sys-kernel/gentoo-sources-5.15.80`.

### Files
 - `lsusb`                      - list of USB devices
 - `lspci`                      - list of PCI devices
 - `dmesg`                      - kernel log from configured kernel
 - `genkernel_dmesg`            - kernel log from generic kernel configured with `genkernel`
 - `genkernel_lsmod`            - module list from generic kernel configured with `genkernel`
 - `ideapad320_15ikb_defconfig` - kernel configuration

### Usage
```
root # cp ideapad320_15ikb_defconfig /usr/src/linux*gentoo/arch/x86/configs/ideapad320_15ikb_defconfig
root # cd /usr/src/linux*gentoo/
root # make ideapad320_15ikb_defconfig
root # make oldconfig
root # make && make install
```

### Useful links
 - [Intel Dual Band network controller](https://wiki.gentoo.org/wiki/Iwlwifi)
 - [NVIDIA discrete graphics](https://wiki.gentoo.org/wiki/NVIDIA/nvidia-drivers)
 - [Intel integrated graphics](https://wiki.gentoo.org/wiki/Intel)
 - [Intel microcode](https://wiki.gentoo.org/wiki/Intel_microcode)
 - [PulseAudio](https://wiki.gentoo.org/wiki/PulseAudio)
 - [Steam](https://wiki.gentoo.org/wiki/Steam)
 - [zswap](https://wiki.gentoo.org/wiki/Zswap)
 - [Lenovo Ideapad 315-ARE05 configuration](https://wiki.gentoo.org/wiki/Lenovo_Ideapad_3_15ARE05_(Ryzen))
 - [Lenovo Ideapad B570e configuration](https://wiki.gentoo.org/wiki/Lenovo_IdeaPad_B570e)
 - [Kernel configuration guide](https://wiki.gentoo.org/wiki/Kernel/Gentoo_Kernel_Configuration_Guide)