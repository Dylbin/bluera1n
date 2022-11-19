<h1 align="center">
    <img src="https://github.com/Dylbin/bluera1n/blob/main/CydiaIcon.png?raw=true" alt="bluera1n logo">
    <p>bluera1n</p>
</h1>
<h3 align="center">An iOS 15.0-15.7.1 work-in-progress, semi-tethered jailbreak based on the checkm8 BootROM exploit.</h3>
<p align="center">
</p>

# How does it work?
It boots the device with multiple patches required. On first run, it'll boot a ramdisk which dumps your onboard SHSH blob, creates a fakefs (if using semi tethered), installs the loader app, and patches your kernel.

### Windows
- no

### Linux
- Linux has some weird usbmuxd issues. We have tried our best to fix them, but there still are issues. We highly recommend to compile and install usbmuxd2.
- Stop making issues about Linux not being able to connect, we are aware. This includes being stuck on waiting for ramdisk to finish booting.

### Warning
- I am **NOT** responsible for any data loss. The user of this program accepts responsibility should something happen to their device. While nothing should happen, jailbreaking has risks in itself. **If your device is stuck in recovery, please run one of the following:**
   - futurerestore --exit-recovery
   - irecovery -n

### A10 and A11 devices
- On A10 and A11, **you must disable your passcode while in the jailbroken state**.
  - On A10 (example: iPhone 7/7 Plus, this can be fixed in the future by implementing blackbird.
  - On A11 (example: iPhone 8/8+/X, we don't have a SEP exploit yet.

# Prerequisites
#### Warning: You must install the Tips app from the App Store before running bluera1n.
- A checkm8 vulnerable iOS device on iOS 15.x (A8-A11)
  - The device must be on iOS 15.0-15.7.1
- Linux or macOS computer
  - Python 3 must be installed.

1. Clone this repo with `git clone --recursive https://github.com/Dylbin/bluera1n && cd bluera1n`
2. Run `./bluera1n.sh --tweaks <your current iOS version>` (run with `sudo` if you're on linux)
   - [A10 and A11] Before running, **you must disable your passcode**.
   - Put your device in DFU mode before running.
3. Follow the steps on your screen.

# Repos

### Tweaks mode
All repos work when using tweaks mode because it uses normal Procursus and not rootless.

### Rootless 
Repos need to be updated for rootless, here are some that work currently:

- [Mineek's repo](https://mineek.github.io/repo) contains rootless Procursus packages

# Credits
- [Nathan](https://github.com/verygenericname)
    - The ramdisk that dumps blobs is a slimmed down version of [SSHRD_Script](https://github.com/verygenericname/SSHRD_Script)
    - For modified [restored_external](https://github.com/verygenericname/sshrd_SSHRD_Script)
    - Also helped Mineek getting the kernel up and running and with the patches
    - Helping with adding multiple device support
    - Fixing issues relating to camera.. etc by switching to fsboot
    - [iBoot64Patcher fork](https://github.com/verygenericname/iBoot64Patcher)
- [Mineek](https://github.com/mineek)
    - For the patching and booting commands
    - Adding tweak support
    - For patchfinders for RELEASE kernels
    - [Kernel15Patcher](https://github.com/mineek/PongoOS/tree/iOS15/checkra1n/Kernel15Patcher)
    - [Kernel64Patcher](https://github.com/mineek/Kernel64Patcher)
- [Amy](https://github.com/elihwyma) for the [Pogo](https://github.com/elihwyma/Pogo) app
- [checkra1n](https://github.com/checkra1n) for the base of the kpf
- [nyuszika7h](https://github.com/nyuszika7h) for the script to help get into DFU
- [the Procursus Team](https://github.com/ProcursusTeam) for the amazing [bootstrap](https://github.com/ProcursusTeam/Procursus)
- [F121](https://github.com/F121Live) for helping test
- [m1sta](https://github.com/m1stadev) for [pyimg4](https://github.com/m1stadev/PyIMG4)
- [tihmstar](https://github.com/tihmstar) for [pzb](https://github.com/tihmstar/partialZipBrowser)/original [iBoot64Patcher](https://github.com/tihmstar/iBoot64Patcher)/original [liboffsetfinder64](https://github.com/tihmstar/liboffsetfinder64)/[img4tool](https://github.com/tihmstar/img4tool)
- [xerub](https://github.com/xerub) for [img4lib](https://github.com/xerub/img4lib) and [restored_external](https://github.com/xerub/sshrd) in the ramdisk
- [Cryptic](https://github.com/Cryptiiiic) for [iBoot64Patcher](https://github.com/Cryptiiiic/iBoot64Patcher) fork, and [liboffsetfinder64](https://github.com/Cryptiiiic/liboffsetfinder64) fork
- [libimobiledevice](https://github.com/libimobiledevice) for several tools used in this project (irecovery, ideviceenterrecovery etc), and [nikias](https://github.com/nikias) for keeping it up to date
- [Nick Chan](https://github.com/asdfugil) general help with patches.
- [Sam Bingner](https://github.com/sbingner) for [Substitute](https://github.com/sbingner/substitute)
