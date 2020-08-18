Work In Progress
# Lian_Yu Writeup

## [Task 1] Find the Flags 
### 1 Deploy the VM and Start the Enumeration.
- Nmap Scan
21/tcp    open  ftp     vsftpd 3.0.2
22/tcp    open  ssh     OpenSSH 6.7p1 Debian 5+deb8u8 (protocol 2.0)
| ssh-hostkey: 
|   1024 56:50:bd:11:ef:d4:ac:56:32:c3:ee:73:3e:de:87:f4 (DSA)
|   2048 39:6f:3a:9c:b6:2d:ad:0c:d8:6d:be:77:13:07:25:d6 (RSA)
|   256 a6:69:96:d7:6d:61:27:96:7e:bb:9f:83:60:1b:52:12 (ECDSA)
|_  256 3f:43:76:75:a8:5a:a6:cd:33:b0:66:42:04:91:fe:a0 (ED25519)
80/tcp    open  http    Apache httpd
|_http-server-header: Apache
|_http-title: Purgatory
111/tcp   open  rpcbind 2-4 (RPC #100000)
| rpcinfo: 
|   program version    port/proto  service
|   100000  2,3,4        111/tcp   rpcbind
|   100000  2,3,4        111/udp   rpcbind
|   100000  3,4          111/tcp6  rpcbind
|   100000  3,4          111/udp6  rpcbind
|   100024  1          36406/tcp6  status
|   100024  1          37077/tcp   status
|   100024  1          42039/udp   status
|_  100024  1          58758/udp6  status
37077/tcp open  status  1 (RPC #100024)
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

- Visiting the Site 
oliver queen 
html
- Source-code
nothing
- Dirbuster
/island
- Source-code
Code Word: vigilante

### 2 What is the Web Directory you found?
/island/2100/
a youtube video
- Source-code
<!-- you can avail your .ticket here but how?   -->

### 3 what is the file name you found?

- Dirbuster 
/green_arrow.ticket

### 4 what is the FTP Password?
### 5 what is the file name with SSH password?
### 6 user.txt
### 7 root.txt
