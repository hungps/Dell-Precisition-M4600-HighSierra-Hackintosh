# Dell Precision m4600 on High Sierra

CLOVER folder for to install MacOS for Dell Precision m4600


### My Specs:

CPU: i7-2620M, 3200 MHz

RAM: 8GB DDR3

Motherboard Chipset: Intel Cougar Point QM67, Intel Sandy Bridge

GPU: Intel HD3000 / NVIDIA Quadro 2000M

Sound: IDT 92HD90BXX

Monitor: Samsung 156AT (Dell C54GW) 15,6" HD

LAN: Intel(R) 82579LM Gigabit Network Connection

WIFI: Intel(R) Centrino(R) Ultimate-N 6300 AGN

### What's working

- Full SpeedStep CPU (using [ssdtPRGen](https://github.com/Piker-Alpha/ssdtPRGen.sh))

- GPU: Intel HD3000 (You can use nVidia by change the smbios to macbookpro9,1 and disable nVidia Optimus but you will lost speedstep and sleep)

- Sound: AppleHDA working using [this patch](https://github.com/insanelydeepak/cloverHDA-for-Mac-OS-Sierra-10.12)

- Keyboard, Touchpad

- Shutdown

- Restart

- Sleep

- Ethernet

- USB2.0, USB3.0

### Not yet working:

- SD Card slot

- Stock Wi-fi card

- Bluetooth (show up but cannot disable, auto disconnect after a few second)

- VGA/HDMI (Not tested)

### Prerequisites

- USB MacOS High Sierra installer

- BIOS: AHCI mode -> SATA

- BIOS: Secure boot -> disabled

- nVidia Optimus -> On

- Your disk should be converted from LEGACY to UEFI (if not) using Minitool Partition

### Install

- Clone/Download this repo and rename the repo's folder to **CLOVER**, and put in boot partition -> *EFI* folder

- Add Clover boot loader file **\EFI\CLOVER\CLOVERX64.efi** to UEFI boot list (in BIOS)

- Boot into Clover, select your USB, create a Mac partition and install MacOS

### Post-install

- Download your favorite kext installer app like [this](http://www.insanelymac.com/forum/files/file/397-easykext-pro-a-minimal-and-super-fast-kext-installer/)

- Download and install newest [VoodooPS2Controller by Dr.Hurt](https://osxlatitude.com/forums/topic/8285-refined-alps-touchpad-driver/) or build it by yourself [here](https://github.com/DrHurt/OS-X-ALPS-DRIVER)

- Download and install [cloverHDA](https://github.com/insanelydeepak/cloverHDA-for-Mac-OS-Sierra-10.12)

- If USB3.0/Battery/Ethernet not working, install ACPIBatteryManager, GenericUSBXHCI, IntelMausiEthernet and restart


_Any pull request would be appreciated_
