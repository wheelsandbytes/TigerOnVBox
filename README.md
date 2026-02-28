# Install Mac OS X 10.4.7 Tiger (Server) on VirtualBox on macOS Monterey

![Screenshot of Tiger VM on Monterey](https://github.com/user-attachments/assets/054b4846-2627-44b1-b92b-758f81880dab)

## Prerequisites
This guide assumes that you have:
- a Mac OS X host environment, running VirtualBox on an Intel Mac
- a universal or i386 install image or disk for Mac OS X 10.4 Tiger

The environment of the example installation procedure was:
 - MacBook Pro (Retina, 15-inch, Mid 2015) - MacBookPro11,5
   - 2.5 GHz Quad-Core Intel Core i7
 - macOS Monterey 12.7.6 (21H1320)
 - VirtualBox 6.1.34 r150636 (download directly from Oracle [here](https://download.virtualbox.org/virtualbox/6.1.34/VirtualBox-6.1.34-150636-OSX.dmg))
 - the Mac OS X Server v10.4.7 (Universal) image ~~(which can be
   found by searching for "10.4" in
   [https://developer.apple.com/download/more/](https://developer.apple.com/download/more/))~~ (which can be found on [Macintosh Repository](https://www.macintoshrepository.org/13602-mac-os-x-server-10-4-7-tiger-))

## Create a new virtual machine

The following step-by-step
procedure will guide you in the creation and configuration of the virtual
machine:

1. select *Machine → New...* from the menu (or click on the *New* button)
2. choose the name of your virtual machine (the example uses "Tiger")
3. select **Type: Mac OS X**
4. select **Version: Mac OS X (32-bit)** or **Version: Mac OS X (64-bit)**
5. choose the amount of RAM (default: 2048 MB)
6. choose *Create a virtual hard disk now*

![Settings for the creation of the virtual machine](images/vm-creation.png)

7. choose the settings for the creation of the virtual hard disk (the default
   ones should work just fine)

![Settings for the creation of the virtual hard disk](images/disk-creation.png)

8. from the command-line, run the following commands (replacing "Tiger" with the
   name of your virtual machine):

```
VBoxManage modifyvm "Tiger" --mouse usb
VBoxManage modifyvm "Tiger" --firmware efi32
VBoxManage modifyvm "Tiger" --cpu-profile 'Intel Pentium 4 3.00GHz'
VBoxManage modifyvm "Tiger" --cpuidset 00000000 00000004 756e6547 6c65746e 49656e69
VBoxManage modifyvm "Tiger" --cpuidset 00000001 00000f43 00020800 fbffffff ffffffff
VBoxManage modifyvm "Tiger" --cpuidset 80000001 00000000 00000000 ffffffff ffffffff
VBoxManage setextradata "Tiger" VBoxInternal/Devices/efi/0/Config/DmiBIOSVersion EFI32..Virtual.Box
VBoxManage setextradata "Tiger" VBoxInternal/Devices/efi/0/Config/DmiUseHostInfo 0
VBoxManage setextradata "Tiger" VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC 1
```

![Expected result](https://github.com/user-attachments/assets/08b18c95-8c10-43bf-88f6-0e982e783b28)

The virtual machine should now be ready for the install procedure. Its `vbox`
file should match the reference [`Tiger.vbox`](Tiger/Tiger.vbox) except for the
name, timestamps and UUIDs.

## Install Mac OS X
1. start the virtual machine
2. since it is the first boot, VirtualBox will open a popup asking for the
   install media; select the Mac OS X install disk image

![Select install media](images/first-boot.png)

3. wait some time for the boot to complete; the system might either immediately
   start or stay frozen for several seconds in a state like the one shown in the
   following image before getting to the UI; after a minute, if it shows no
   progress or if the console shows `Still waiting for root device.`, try
   rebooting the machine

![Boot wait](images/boot-wait.png)

4. choose the language you are going to use

![Language selection](images/language.png)

5. from the hidden menu at the top of the screen, select *Utilities → Disk
   Utility...*

   **IMPORTANT**: open *Disk Utility* **immediately** after selecting the
   language. Stepping through the installation and then running *Disk Utility*
   will likely result in the hard disk not being shown.

![Open Disk Utility](images/utilities-du.png)

6. erase the *VBOX HARDDISK* hard disk using a **Mac OS Extended** volume
format; you can choose whether to also make it Journaled and/or Case-sensitive;
the default is *Mac OS Extended (Journaled)*

![Erase the hard disk](images/du-erase.png)

7. quit *Disk Utility* and proceed with the installation

## Additional information
* [Post-installation tuning](Tuning.md)
* [Known issues](Issues.md)
* [Explanation of the settings](Explanation.md)
