# Common Linux Privesc Writeup

## [Task 1 - 3]

Follow The Readings Provided

## [Task 4] Enumeration

### 1 SSH into machine with the provided credentials 

username = user3
password = password

- ssh user3@10.10.x.x
![1](https://user-images.githubusercontent.com/69840849/90487228-85318c80-e17d-11ea-97a6-4fae52b8f968.png)

### 2 What is the target's hostname?

- hostname
![1](https://user-images.githubusercontent.com/69840849/90487310-a4c8b500-e17d-11ea-8c13-e124db0080e5.png)
 
### 3 Look at the output of /etc/passwd how many "user[x]" are there on the system?

- cat /etc/passwd
![1](https://user-images.githubusercontent.com/69840849/90487951-7f887680-e17e-11ea-9a89-695bbae5f50e.png)

### 4 How many available shells are there on the system?

- cat /etc/shells
![1](https://user-images.githubusercontent.com/69840849/90487873-654e9880-e17e-11ea-930b-d8a76d45b608.png)

### 5 What is the name of the bash script that is set to run every 5 minutes by cron? 

- cat /etc/crontab
[!] You should be able to find the name of the .sh file
![1](https://user-images.githubusercontent.com/69840849/90487765-405a2580-e17e-11ea-917b-2c482e84784c.png)

### 6 What critical file has had its permissions changed to allow some users to write to it?

- ls -la /etc/passwd
![1](https://user-images.githubusercontent.com/69840849/90488017-9929be00-e17e-11ea-8e7b-2a970579333e.png)

### 7 Enumeration Completed

## [Task 5] Abusing SUID/GUID Files

## [Task 6] Exploiting Writeable /etc/passwd 

## [Task 7] Escaping Vi Editor 

## [Task 8] Exploiting Crontab 

## [Task 9] Exploiting PATH Variable 

## [Task 10] Expanding Your Knowledge 
