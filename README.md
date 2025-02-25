# Lenovo Ideapad 320-15IKB

Kernel configuration for [Lenovo Ideapad 320-15IKB \(Type 80XL\) laptop](pcsupport.lenovo.com/us/en/products/laptops-and-netbooks/300-series/320-15ikb/)

This is an educational project. It is created to master kernel configuration skills and potentially learn how to configure the kernel in bottom-up rather then in top-down manner. The quality of the configuration is not guaranteed.

### Methodology
The end goal is to create an all-in-one-file kernel. The steps:

 1. [ ] Take a configuration from *genkernel*.
 2. [ ] Transfer the configuration to *zen* and run *oldconfig*, optimize for native processor
 3. [ ] Test (test result: N/A)
 4. [ ] Strip down unneeded modules
 5. [ ] Test (test result: N/A)
 6. [ ] Compile-in modules
 7. [ ] Test (test result: N/A)
 8. [ ] Compile-in firmware
 9. [ ] Test (test result: N/A)
 10. [ ] Disable initramfs
 11. [ ] Test (test result: N/A)

### Testing protocol
The things that most commonly go wrong and therefore must be tested extensively:
 - Suspend to RAM
 - Suspend to disk
 - Wired network
 - Wi-Fi network
 - Touchpad, mouse and keyboard
 - Battery
 - Beeper
 - Speakers
 - Camera
 - Microphone (presence of the microphone device, the quality of the sound is off question)
 - Dedicated video card (`prime-run` and `nvidia-smi`)
 - Connection to Android devices
 - (to be continued)

### Files
 - `lsusb`                         - list of USB devices
 - `lspci`                         - list of PCI devices
 - `dmesg`                         - kernel log from configured `gentoo` kernel
 - `genkernel_dmesg`               - kernel log from generic kernel configured with `genkernel`
 - `genkernel_lsmod`               - module list from generic kernel configured with `genkernel`
 - `ideapad320_15ikb_defconfig`    - configuration of `gentoo-sources-5.15.80` kernel
 - `ideapad320_15ikb_zen_defconfig`- configuration of `zen-sources-6.2.13` kernel (same as `gentoo` but with native optimization)

### Log
The changes of the configuration are to be noted here:
 - Disable virtualization
 - Disable systemd support
 - Select NFTS as the NTFS driver
 - Enable Intel-native optimizations

### Useful links
 - [Xorg](https://wiki.gentoo.org/wiki/Xorg/Guide)
 - [Intel Dual Band network controller](https://wiki.gentoo.org/wiki/Iwlwifi)
 - [NVIDIA discrete graphics](https://wiki.gentoo.org/wiki/NVIDIA/nvidia-drivers)
 - [Intel integrated graphics](https://wiki.gentoo.org/wiki/Intel)
 - [Intel microcode](https://wiki.gentoo.org/wiki/Intel_microcode)
 - [Power management](https://wiki.gentoo.org/wiki/Power_management/Guide)
 - [PulseAudio](https://wiki.gentoo.org/wiki/PulseAudio)
 - [Steam](https://wiki.gentoo.org/wiki/Steam)
 - [zswap](https://wiki.gentoo.org/wiki/Zswap)
 - [elogind](https://wiki.gentoo.org/wiki/Elogind)
 - [PPP](https://wiki.gentoo.org/wiki/PPP)
 - [CryFS](https://packages.gentoo.org/packages/sys-fs/cryfs) (requires CONFIG_FUSE_FS)
 - [Cryptsetup](https://packages.gentoo.org/packages/sys-fs/cryptsetup) (requires CONFIG_DM_CRYPT)
 - [AVR](https://wiki.gentoo.org/wiki/Arduino)
 - [Lenovo Ideapad 315-ARE05 configuration](https://wiki.gentoo.org/wiki/Lenovo_Ideapad_3_15ARE05_(Ryzen))
 - [Lenovo Ideapad B570e configuration](https://wiki.gentoo.org/wiki/Lenovo_IdeaPad_B570e)
 - [Kernel configuration guide](https://wiki.gentoo.org/wiki/Kernel/Gentoo_Kernel_Configuration_Guide)
