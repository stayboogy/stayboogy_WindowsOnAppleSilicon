# stayboogy_WindowsOnMacOS

how to get a proper working Windows 10 Arm64 VM install working with sharing

## Windows 10 Arm64 VM on M1 Macbook Pro

1) install VMware Fusion 13.5

	- UTM has some kind of hardcoded 4GB filesize limit when sharing files and in Windows 10 Arm64 for some reason, and is a waste of time
	
	- VMWare Fusion Requires Free Registration at VMWare
	
	- Download Link Here for Convenience 
	 
https://www.mediafire.com/file/lferq3q9mpfknfb/VMware-Fusion-13.5.0-22583790_universal.dmg/file
	
		

2) download the proper Windows Insider 21390.1 Build for Multi Arm64

	- Untouched ISO direct from ESD Download
	
	- Asks for Key on Install - not needed
	
	- Expired Build - Update Nag Screen at Every Boot
	
	- No Other Issues - Can use in Perpetuity
	
	- Download Link Here for Convenience
	
https://www.mediafire.com/file/0ezcck3ka5j6b3c/21390.1_MULTI_ARM64_EN-US.ISO/file
	
	
3) Install Windows 10 in VMWare Fusion

	- Create a Custom Virtual Machine
	
	- Choose Windows 11 Arm64 - even though we are using 10
	
	- Choose UEFI with NO Secure Boot
	
	- Create a password when it asks for one for the TPM 2.0 module emulation
	
	- All Other Settings you can choose as necessary
	
	- Install as normal
	
	- Activate VL with KMS (see https://msguides.com/windows-10 for a no extra software or malware way to do this)
	
	- Install VMWare Tools for Windows, Reboot
	
	
4) Make sure Networking is NOT Using NAT / sharing connnection with this Mac

	- Networking needs to have a seperate presence on the network to have file sharing working
	
	![App Screenshot](https://codeberg.org/stayboogy/stayboogy_WindowsOnMacOS/raw/branch/main/network.png)
	
	- File Sharing can only be done directly through SMB
	
	- In Windows, right-click and "Give Access to" and give yourself access to the folders you want to share from Windows
	
	- In Windows, turn off Windows Defender Firewall
	
	- In Windows, Control Panel, Advanced Networking and Sharing, turn on password protected sharing for all networks
	
	- In Windows, make sure you have a password set for your login, empty passwords will not work for MacOS smb sharing
	
	- Reboot your Windows VM, and sign in
	
	- In MacOS, Finder, Go, Connect to Server, the ip of the Windows VM, Windows username and password
	
	- Enjoy your Proper Windows 10 Arm64 VM