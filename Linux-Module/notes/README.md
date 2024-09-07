# Linux notes

Basic Linux Commands
•	/root – user directory for the root user
•	/tmp – temporary files
•	/boot – system boot loader files
•	mkdir – use mkdir command to make a new directory
•	rmdir – use this command to delete directories and the contents within them
•	ls – view content of a directory
•	mv – to move files
•	locate – locate a file is a search command
•	cp – copy files from current directory to different directory

What is Linux? 
-	Open-source operating system
-	Founded by Linus

Benefit of Virtualisation? 
-	Allows you to run Linux on your existing computer without needing to replace your current OS.
-	Allows you to run an entire OS from your own computer
-	Allows multiple OS to run on a single physical machine
-	They share resources but remain isolated from each other


Head & Tail command:
- powerful tool to show begninning and end of files by specifying the lines to display
example: head -n 10 multiline.txt | tail -n 5 
example 1: 
man cat 
touch multiline.txt   
vim multiline.txt 
head multiline.txt   







Challenge for me:

Create a script that updates the security group for every period that your IP changes.

1. Curl command to get your IP
2. Having AWS cli configured
3. AWS commands to update SSH Port 22 in security group to whitelist your new IP
4. Now the security group has your new IP, so you can SSH successfully
5. Automate the script to run every hour using Crontab (0 * * * *)


Use below command regularly to check my public IP. It changes once in a while:
- curl http://checkip.amazonaws.com/'
