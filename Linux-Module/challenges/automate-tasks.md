Challenge for me:

Create a script that updates the security group for every period that your IP changes.

1. Curl command to get your IP
2. Having AWS cli configured
3. AWS commands to update SSH Port 22 in security group to whitelist your new IP
4. Now the security group has your new IP, so you can SSH successfully
5. Automate the script to run every hour using Crontab (0 * * * *)


Useful commands:

Use below command regularly to check my public IP. It changes once in a while:
- curl http://checkip.amazonaws.com/'


Network challenge:

create an EC2 instance with nginx hosted on it
create an A record on Cloudflare and point it to your EC2 IP. make sure to have port 80 open btw. the A record name will be "nginx" and value will be your EC2 IP

now when you have done that, i want to be able to access the home nginx webpage on nginx.AbuTekky.com