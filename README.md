# deep-learning-setup-5820

Steps to get started and install necessary tools on Dell Precision 5820 Tower. Windows 10 was already installed
by the vendor. Dual is required to have both Ubuntu and Windows. This guide can also be followed to install 
Ubuntu alone. **Ubuntu 18.04 LTS** is used here.

### Dual Boot, Ubuntu 18.04
Follow the steps below to make it dual boot

1.  Disable the secure boot option in BIOS. Follow [this](https://fossbytes.com/enable-disable-secure-boot-windows-8-10/)
for step by step process.
2.  Download **Ubuntu 18.04 Desktop** from [here](https://releases.ubuntu.com/18.04.5/ubuntu-18.04.5-desktop-amd64.iso). 
Download **Rufus** from [here](https://rufus.ie/) to make a bootable USB. Note that you have to select
`GPT` in the `Partition scheme`.
3.  Change the boot mode from `UEFI` to `Legacy`. Insert the bootable USB and restart. When `DELL` is flashed 
on the screen, frequently press `F12` to enter the boot menue. From here select proper USB name, e.g. Kingston
to start installation.
4.  At this moment you will see selection screen for installing Ubuntu. Select `install Ubuntu` and hit `e` to 
edit the boot options. Add `nomodeset` before `---` and hit `F10`. Now normal installation for Ubuntu will start.
Select options that suits you.
5.  After successfull installation restart the computer. There might be some crashing of display due to drivers
but please don't panic. Put the computer in `sleep mode` and than wake it up again. Now you will see the login
screen.

### Nvidia Drivers & CUDA Toolkit
Install `NVIDIA drivers` by following the instructions given [here](https://docs.nvidia.com/cuda/archive/11.0/cuda-installation-guide-linux/index.html). Along
with drivers this process will also install `cuda 11.0`. Now install `cuda-toolkit` using command `sudo apt install nvidia-cuda-toolkit`.

### PyCharm
Install PyCharm using `sudo snap install pycharm-community --classic`. This will install the latest available
version. Run `PyCharm` from applications and perform settings as you like.

### Anaconda installation
For installing anaconda follow the steps explained [here](https://docs.anaconda.com/anaconda/install/linux/)

