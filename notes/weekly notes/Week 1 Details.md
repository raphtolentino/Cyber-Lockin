
## Week 1 : Day 1

Daily Goals:
- [x] Setup Github Repo
- [x] Download and Install Github Desktop
- [x] Download VirtualBox and Install it
- [x] Download VM's iso (Kali Linux, Ubuntu Server, Windows 10) and install it
- [x] Download Windows Server 2025 + Ubuntu iso for later projects.

### Project Setup:

- Setup the GitHub repo for this project.
![[github_setup.png]]

This project file structure is as following:
	1. Notes:
		1. Weekly notes
		2. Weekly Notes Screenshots
	2. Config_files
		1. vm_files
	3. Other
	4.  License (MIT)
	5. README.md
	
- Dowloaded GitHub Desktop and installed on my local Desktop

Website link: https://desktop.github.com/download/

![[Pasted image 20250925111949.png]]
- Cloned the repository 

![[Pasted image 20250925112042.png]]

- Downloaded VirtualBox Exe file, Executed the EXE and Installed on my local SSD drive.

Website link: https://www.virtualbox.org/wiki/Downloads

![[Pasted image 20250925113328.png]]
- Downloaded Operating Systems ISO's

kali_linux: https://www.kali.org/get-kali/#kali-virtual-machines
ubuntu:   https://ubuntu.com/download/server
windows 10: https://www.microsoft.com/en-gb/software-download/windows10
windows server; https://info.microsoft.com/ww-landing-evaluate-windows-server-2025.html?lcid=en-us&culture=en-us&country=us

- Created a Virtual Machine for each OS. With a selective configuration settings:
Kali/Windows 10/ Ubuntu Server Configuration:
	Virtual Machine Settings:
		 2 CPU Cores
		 2040MB RAM
		 50GB HDD Storage
		 Audio Enabled
	 Network Details:
		Adapter Name : NAT Network
			IP range: 192.168.0.0/24
		Adapter Name: Host-Only Network
			IP address: 192.168.137.1


## Week 1: Day 2

Daily Goals:
- [ ] Check VM's Ip addresses
- [ ] Ping all 3 VM's with each other
- [ ] SSH from Kali/Windows 10 into Ubuntu Server
- [ ] Create a file on Ubuntu Server and edit using NANO

### Check VM's Ip addresses

How to check IP addresses within the OS terminal.

Linux:
```
ip a
```
Windows:
```
ipconfig
```

Kali: 
![[Pasted image 20250925115025.png]]
Ubuntu Server:
![[Pasted image 20250925115259.png]]
Windows 10:

 ### Ping all 3 VM's with each other

Kali to Ubuntu:
```
ping 10.0.0.5 -c 4
```
![[Pasted image 20250925115419.png]]

Kali to Windows 10
```
ping 10.0.0.4 -c 4
```

![[Pasted image 20250925121242.png]]

Ubuntu to Kali

```
ping 10.0.0.5 -c 4
```

![[Pasted image 20250925115708.png]]
Ubuntu to Windows 10

```
ping 10.0.0.4 -c 4
```

![[Pasted image 20250925121358.png]]

Windows to Kali

```
ping 10.0.0.3 -c 4
```

![[Pasted image 20250925121646.png]]

Windows to Ubuntu 



SSH from Kali/Windows 10 into Ubuntu Server














