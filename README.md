# Hackintosh Build 
**Current version: (v.10.9.1)**

### Hardware:

* Z77-DS3H
* i5-3570K @ 4.3GHz
* 2x8 DDR3 Corsair Vengeance
* ATI HD 5850


## Step by Step

### 0. Set BIOS settings
* set hard disk in AHCI mode.

![](https://raw.github.com/Kikobeats/hackintosh/master/0.%20BIOS%20/1%20-%20ahci%20mode.png)

* set memories in Profile1 (1600 MHz)

![image](https://raw.github.com/Kikobeats/hackintosh/master/0.%20BIOS%20/2%20-%20mem%20profile.jpg)

* set yout CPU overlock and disable EIST



![image](https://raw.github.com/Kikobeats/hackintosh/master/0.%20BIOS%20/3%20-%20overclock.jpg)


### 1. Install latest version of Mavericks (Obvious)

* [myHack](http://myhack.sojugarden.com/guide/) for create USB installer and remove useless kexts

### 2. Install custom kexts

* [Multibeast 6.0.1](http://www.tonymacx86.com/downloads.php?do=file&id=206)
* Custom settings for Z77-DS3H:

![image](https://raw.github.com/Kikobeats/hackintosh/master/2.%20Custom%20Kexts/settings.png)

	
I recommend you have 2 bootloaders: First, Chimera, and later install Clover (EFI). You run your computer normally with Clover and if you need repair anything you can use chimera for emergency.

### 3. Install EFI Bootloader

Clover is better Bootloader than Chimera. more information [here](http://kikobeats.apps.runkite.com/clover-efi-bootloader/)

*  Install [Clover](http://sourceforge.net/projects/cloverefiboot/) with this settings:

	* UEFI Install
	* Install to ESP
	* Choose all themes
	* Choose UEFI 64 bit drivers: DataHubDxe-64, EMUVariableUEFI-64 and OSXAptioFixDrv-64  
	* Install RC Scripts
	* Install Optional RC Scripts
	* Install Clover Preference Pane
	
Once you install make sure you create a config.plist by going to terminal and entering this code: 

	/usr/local/bin/clover-genconfig >config.plist
	
You will then have to tweak it a little based on your system and preferences - see various Clover resources for "How To"

* Install your Ivybridge SSDT and if you like a custom DSDT in EFI/Clover/ACPI/Patched

* Mount EFI partition:

		diskutil list
		mkdir /Volumes/efi
		sudo mount -t msdos /dev/diskXsX /Volumes/efi


* more information [here](http://www.tonymacx86.com/mavericks-desktop-guides/114133-mavericks-install-ga-z77-ds3h-w-gt640.html).


### 4. Install utilities

* [Kext Wizard](http://dl.dropboxusercontent.com/u/7085278/Kext_Wizard/download.html)
* [Kext Utility](http://cvad-mac.narod.ru/index/0-4)





