# stayboogy_WindowsOnMacOS

how to get a proper working Windows 10 Arm64 VM install working with sharing

## Windows 10 Arm64 VM on M1 Macbook Pro

1) install VMware Fusion 13.5

	- UTM does not work properly with file sharing and writing to the virtual disk and is a waste of time
	
	- Requires Free Registration at VMWare
	
	- Download Link Here for Convenience 
	 
https://www.mediafire.com/file/lferq3q9mpfknfb/VMware-Fusion-13.5.0-22583790_universal.dmg/file
	
		

2) download the proper Windows Insider 21390.1 Build for Multi Arm64

	- Untouched ISO direct from ESD Download
	
	- Asks for Key on Install - not needed
	
	- Expired Build - Update Nag Screen at Every Boot
	
	- No Other Issues - Can use in Perpetuity
	
	- Download Link Here for Convenience
	
https://www.mediafire.com/file/0ezcck3ka5j6b3c/21390.1_MULTI_ARM64_EN-US.ISO/file
	
	
3) Make sure Networking is NOT Using NAT / sharing connnection with this Mac

	- Networking needs to have a seperate presence on the network to have file sharing working
	
	- File Sharing can only be done directly through SMB
	
	- In Windows, right-click and "Give Access to" and give yourself access to the folders you want to share from Windows
	
	- In Windows, turn off Windows Defender Firewall
	
	- In Windows, Control Panel, Advanced Networking and Sharing, turn on password protected sharing for all networks
	
	- In Windows, make sure you have a password set for your login, empty passwords will not work for MacOS smb sharing
	
	- Reboot your Windows VM, and sign in
	
	- In MacOS, Finder, Go, Connect to Server, the ip of the Windows VM, Windows username and password
	
	- Enjoy your Proper Windows 10 Arm64 VM