# Common Linux Privesc

## Task 1 - 3

Follow Readings

## Task 4 Enumeration

### 1 SSH into machine with the provided credentials 

username = user3
password = password

- ssh user3@10.10.x.x
![1](https://user-images.githubusercontent.com/69840849/90487021-3683f280-e17d-11ea-92b6-a03a6ba4ffdd.png)

### 2 What is the target's hostname?

- hostname
 
### 3 Look at the output of /etc/passwd how many "user[x]" are there on the system?

- cat /etc/passwd

### 4 How many available shells are there on the system?

- cat /etc/shells

### 5 What is the name of the bash script that is set to run every 5 minutes by cron? 

- cat /etc/crontab
[!] You should be able to find the name of the .sh file

### 6 What critical file has had its permissions changed to allow some users to write to it?

- ls -la /etc/passwd

### 7 Enumeration Completed

