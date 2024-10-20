# Bandit-overthewire

This repository contains writeup for solving Bandits - Tanisha Mathur
### Login/ LEVEL 0
To connect to the host and the port, use the command –
ssh bandit0@bandit.labs.overthewire.org -p2220
The password to enter into the level 0 is bandit0.
We use the ls command to list the files in the head directory. Use cat command that concatenates or can be used to display the content of a file.
Command used: cat readme
We use exit command to exit the level.
![image](https://github.com/user-attachments/assets/0acfb2da-f23b-4596-b851-2aedd228fb03)


 
### LEVEL 1
ssh bandit1@bandit.labs.overthewire.org -p2220
In this level, directly specifying the filename is not going to work as - in Linux refers to Standard Input/Standard output. Hence, we use < to specify the absolute path to the file.
Commands used-  
 ls        cat<-     	exit
 
### LEVEL 2
ssh bandit2@bandit.labs.overthewire.org -p2220
In a command, spaces indicate a new addition to the command. Hence we use single or double quotes to mention a file that has spaces in its name.
Commands used -
  ls 	cat “spaces in this filename”   	exit
 
 ### LEVEL 3
ssh bandit3@bandit.labs.overthewire.org -p2220
To shift to the inhere directory, we use cd command. -hal lists all human readable files and the hidden ones too. Cat is then used to print the required file. Exit command is used to logout from the level.
Commands used – ls 	cd inhere 	ls -hal    cat .hidden   	exit

 
 
### LEVEL 4
ssh bandit4@bandit.labs.overthewire.org -p2220
File command returns the type of data that is found in the file and we can use ‘*’, which is called a ‘wildcard symbol’, it means search all files in the directory. We then use cat to print the required human readable file written in ASCII text.
Commands used – ls	cd inhere 	file ./*  	cat ./-file07    	exit
 
 


### LEVEL 5
ssh bandit5@bandit.labs.overthewire.org -p2220
Here, we use cd command to move to the inhere directory and then find command to find the required file. (.) represents current directory , -type f indicates that we are looking for a file, -not -executable indicates the file that is not executable and -size 1033c means file that occupies the size of 1033 bytes.
Commands used – ls   cd inhere    find . -type f -not -executable -size 1033c   cat
 
 
 ### LEVEL 6
ssh bandit6@bandit.labs.overthewire.org -p2220
find command is used to find the file, directory, etc. that we are looking for.                -type f command determines that we want to find a file, -user and -group defines files owned by the user bandit7 and  the group bandit6 respectively.    	-size denotes the size of the file and 33c means 33 bytes. However, permission denied errors appear so we append 2>/dev/null, which will hide all error messages.
Commands used – find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null    	exit
 
 
 ### LEVEL 7
ssh bandit7@bandit.labs.overthewire.org -p2220
Here we use grep command to get the lines that have a particular pattern , like here the word millionth. With the pipe (|), we can pipe the output of cat to grep as input to look through a text file.
Commands used – ls 	cat data.txt | grep millionth   	exit
 
 
### LEVEL 8
ssh bandit8@bandit.labs.overthewire.org -p2220
uniq is used to filter the input based on identical lines. The command sort is used with uniq as lines need to be sorted first before filtering. -u is a flag that filters lines that appear only once.
The commands used are: ls    	 sort data.txt | uniq -u          	exit
 
 
### LEVEL 9-
ssh bandit9@bandit.labs.overthewire.org -p2220
The strings command finds human-readable strings in files and prints sequences of printable characters. We want to filter that output by looking at lines that include more than one equal sign. For this purpose, we use grep and shall add =  (since number of = is not mentioned , here I hv added 3 ).
Commands used- ls 	strings data.txt | grep ===      	exit
 
 
### LEVEL 10
ssh bandit10@bandit.labs.overthewire.org -p2220
Here the password in encoded and we can use base64 to encode/decode data and print to standard output. Base64 is a binary-to-text encoding scheme. The -d flag is used to decode the data.
Commands used – ls  cat data.txt  	base64 -d data.txt  	exit
 
 
 
 
 
 

