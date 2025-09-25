
### Week 1: Fundamentals

Daily Goals:
1. [x] Setup Github Repo
2. [x] Download & Install VirtualBox
3. [x] Download & Install VM's (Kali Linux, Ubuntu Server, Windows 10).
4. [x] Download Windows Server 2025 + Ubuntu Linux iso for later projects.
5. [x]  Write findings and document every major change.


#### 1: Setup Github Repo

I created a github repo for this project:
<img width="822" height="388" alt="image" src="https://github.com/user-attachments/assets/037e8836-67c6-4d8c-9a30-ae0b710444aa" />

This project file structure will be as following.
	Notes:
		weekly_notes
		screenshots
		readme.md
	config_files
		vm_files
		readme.md
	Other
	License
	README.md
		
--- 
#### 2 : Download & Install VirtualBox
For step 2; I Downloaded VirtualBox Exe file, Executed the EXE and Installed on my local SSD drive.
Website link: https://www.virtualbox.org/wiki/Downloads

<img width="936" height="283" alt="image" src="https://github.com/user-attachments/assets/3d699541-2f70-4d29-9456-c32e61b3cf70" />


---
#### 3. Download & Install VM's (Kali Linux, Ubuntu Server, Windows 10).
With VirtualBox running on my local desktop. I installed - Downloaded Operating Systems ISO's  on these websites.

1. kali_linux: https://www.kali.org/get-kali/#kali-virtual-machines
2. ubuntu:   https://ubuntu.com/download/server
3. windows 10: https://www.microsoft.com/en-gb/software-download/windows10
4. windows server; https://info.microsoft.com/ww-landing-evaluate-windows-server-2025.html?lcid=en-us&culture=en-us&country=us
5. https://ubuntu.com/download/desktop

VM's Hardware Configurations && Network Details

Hardware Configurations:
	CPU: 2 Cores
	RAM: 2GB
	HDD: 50GB

Network Configurations:
	Adapter 1 Name : NAT Network
	Adapter  2 Name: Host-Only Network

--- 
#### 4. Download Windows Server 2025 + Ubuntu Linux iso for later projects.

<img width="734" height="396" alt="image" src="https://github.com/user-attachments/assets/a67b258d-a4e6-4932-aaec-a9bd6df6f212" />


---

#### 5. Write findings and document every major change.

DONE

---

### Week 1: Day 2

1. [x]  Check VM's Ip addresses (Kali Linux, Ubuntu Server, Windows 10)
2. [x]   Create a folder & textfile on Ubuntu Server and edit using commands.
3. [x]  Ping all 3 VM's with each other
4. [x] SSH from Kali/Windows 10 into Ubuntu Server + Access created txt file

--- 
#### 1. Check VM's Ip addresses (Kali Linux, Ubuntu Server, Windows 10)

Commands:

Linux:
``` shell
ip a
```
Windows:
``` bash
ipconfig
```

Virtual Machine Internet Protocol Addresses:
``` markdown
IP's
KALI: 10.0.0.3
Ubuntu: 10.0.0.5
Win10: 10.0.0.4
```

Screenshots
1. Kali Linux
<img width="915" height="296" alt="image" src="https://github.com/user-attachments/assets/4db5e8bc-e51a-4c45-8224-395e6b49bde3" />


2. Ubuntu Server
<img width="922" height="364" alt="image" src="https://github.com/user-attachments/assets/be680e20-152f-48ba-96bd-cea8a1ff5779" />


3. Windows 10 
<img width="927" height="486" alt="image" src="https://github.com/user-attachments/assets/d7b3b4fa-0d87-4c93-bde7-0c50f4f0d7e2" />

--- 
#### 2. Create a folder & text file on Ubuntu Server and edit using commands.

Commands used
``` sh
# this creates a folder and change directory into the folder.
mkdir txt_files && cd txt_files 
# this creates a empty txt file called txt1
touch txt1.txt
# this opens the nano text editor.
nano txt1.txt
# this reads the text file
cat txt1.txt
```

--- 

#### 3.  Ping all 3 VM's with each other

1. Kali -> Ubuntu Server/Windows 10
Kali to Ubuntu Server
```sh
┌──(kali㉿kali)-[~]
└─$ ping 10.0.0.5 -c 4
PING 10.0.0.5 (10.0.0.5) 56(84) bytes of data.
64 bytes from 10.0.0.5: icmp_seq=1 ttl=64 time=2.46 ms
64 bytes from 10.0.0.5: icmp_seq=2 ttl=64 time=1.58 ms
64 bytes from 10.0.0.5: icmp_seq=3 ttl=64 time=1.06 ms
64 bytes from 10.0.0.5: icmp_seq=4 ttl=64 time=1.54 ms

--- 10.0.0.5 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3070ms
rtt min/avg/max/mdev = 1.058/1.659/2.460/0.505 ms

```

Kali to Windows 10:

```sh
┌──(kali㉿kali)-[~]
└─$ ping 10.0.0.4 -c 4
PING 10.0.0.4 (10.0.0.4) 56(84) bytes of data.
64 bytes from 10.0.0.4: icmp_seq=1 ttl=128 time=3.69 ms
64 bytes from 10.0.0.4: icmp_seq=2 ttl=128 time=1.87 ms
64 bytes from 10.0.0.4: icmp_seq=3 ttl=128 time=6.20 ms
64 bytes from 10.0.0.4: icmp_seq=4 ttl=128 time=1.37 ms

--- 10.0.0.4 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss, time 3034ms
rtt min/avg/max/mdev = 1.366/3.283/6.200/1.893 ms


```

2. Ubuntu Server -> Kali Linux/Windows 10 

Ubuntu -> Kali

```sh
root user@root server : ping 10.0.0.5 -c 4
PING 10.0.0.5 (10.0.0.5) 56(84) bytes of data.
64 bytes from 10.0.0.5: ttI=64 time-0.051 ms
64 bytes from 10.0.0.5: tt 1=64 time-0.084 ms
64 bytes from 10.0.0.5: icmp_seq=3 tt 1=64 time=0.048 ms
64 bytes from 10.0.0.5: icmp_seq=4 tt 1=64 time=0.047 ms

--- 10.0.0.5 ping statistics ---
4 packets transmitted, 4 received, packet loss, time 3101ms
rtt min/avg/max/mdev = 0.047/0.057/0.084/0.015 ms

```

Ubuntu -> Windows 10:

```shell
ping 10.0.Ø.4 -c 4
PING 10.0.0.4 (10.0.0.4) 56(84) bytes of data.
64 bytes from 10.Ø.Ø.4: icmp_seq=l ttl=128 time=2.48 ms
64 bytes from 10.Ø.Ø.4: icmp_seq=2 ttl=128 time-I.85 ms
64 bytes from 10.Ø.Ø.4: icmp_seq=3 ttl=128 time-I .03 ms
64 bytes from 10.0.Ø.4: icmp_seq=4 ttl=128 time-I .02 ms
--- 10.0.Ø.4 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss,time 3005ms
rtt min/avg/max/mdev = 1.024/1.611/2.478/0.536 ms
```

3. Windows 10
Windows 10 -> Kali

```bash 
C:\Users\rootuser>ping 10.0.0.3
Pinging 10.0.0.3 with 32 bytes of data:                                                 Reply from 10.0.0.3: bytes=32 time=1ms TTL=64                                           Reply from 10.0.0.3: bytes=32 time=3ms TTL=64                                           Reply from 10.0.0.3: bytes=32 time=2ms TTL=64                                           Reply from 10.0.0.3: bytes=32 time=1ms TTL=64                                                                                                                                   Ping statistics for 10.0.0.3:                                                           Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),                                    Approximate round trip times in milli-seconds:                                          Minimum = 1ms, Maximum = 3ms, Average = 1ms   
```

Windows 10 -> Ubuntu Server
```bash 
C:\Users\rootuser>ping 10.0.0.5 
Pinging 10.0.0.5 with 32 bytes of data:
Reply from 10.0.0.5: bytes=32 time=2ms TTL=64
Reply from 10.0.0.5: bytes=32 time=2ms TTL=64
Reply from 10.0.0.5: bytes=32 time=1ms TTL=64
Reply from 10.0.0.5: bytes=32 time=2ms TTL=64
  
Ping statistics for 10.0.0.5:
Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds:
Minimum = 1ms, Maximum = 2ms, Average = 1ms 
```

---
#### 4. SSH from Kali/Windows 10 into Ubuntu Server + Access created txt file

Kali -> Ubuntu Server

``` sh
┌──(kali㉿kali)-[~]
└─$ ssh rootuser@10.0.0.5
rootuser@10.0.0.5's password: 
Welcome to Ubuntu 24.04.3 LTS (GNU/Linux 6.8.0-84-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Thu 25 Sep 19:16:46 UTC 2025

  System load:  0.23               Processes:               132
  Usage of /:   61.3% of 11.21GB   Users logged in:         1
  Memory usage: 26%                IPv4 address for enp0s3: 10.0.0.5
  Swap usage:   0%


Expanded Security Maintenance for Applications is not enabled.

2 updates can be applied immediately.
1 of these updates is a standard security update.
To see these additional updates run: apt list --upgradable

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


Last login: Thu Sep 25 19:16:28 2025 from 10.0.0.3
rootuser@rootserver:~$ cd txt_files/
rootuser@rootserver:~/txt_files$ ls
text1.txt  txt_files
rootuser@rootserver:~/txt_files$ cat text1.txt 
this is a edit file

rootuser@rootserver:~/txt_files$ exit
```

Windows 10
```bash 
Microsoft Windows [Version 10.0.19045.3803]
(c) Microsoft Corporation. All rights reserved. 
C:\Users\rootuser>ssh rootuser@10.0.0.5
The authenticity of host '10.0.0.5 (10.0.0.5)' can't be established. 
ECDSA key fingerprint is SHA256:EZfQnR3P5BHLrTPbWpXbCAgjz9coseqFudxkE00MdZk.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.0.0.5' (ECDSA) to the list of known hosts. rootuser@10.0.0.5's password:                                                           Welcome to Ubuntu 24.04.3 LTS (GNU/Linux 6.8.0-84-generic x86_64)
* Documentation:  https://help.ubuntu.com
* Management:     https://landscape.canonical.com
* Support:        https://ubuntu.com/pro                                                System information as of Thu 25 Sep 19:33:49 UTC 2025                                   System load:  0.42               Processes:               129 
Usage of /:   61.4% of 11.21GB   Users logged in:         1                             Memory usage: 24%                IPv4 address for enp0s3: 10.0.0.5                      Swap usage:   0%                                                                        

Expanded Security Maintenance for Applications is not enabled.                          2 updates can be applied immediately.
1 of these updates is a standard security update.                                       To see these additional updates run: apt list --upgradable                              

Enable ESM Apps to receive additional future security updates.                          See https://ubuntu.com/esm or run: sudo pro status                                      

Last login: Thu Sep 25 19:16:46 2025 from 10.0.0.3                                                                                                          rootuser@rootserver:~$ cd txt_files/
rootuser@rootserver:~/txt_files$ ls                                                     text1.txt  txt_files  
rootuser@rootserver:~/txt_files$ cat text1.txt                                          this is a edit file                                                                     rootuser@rootserver:~/txt_files$ 
```
