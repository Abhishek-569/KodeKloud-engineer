# Question (Create a Cron Job)
The Nautilus system admins team has prepared scripts to automate several day-to-day tasks. They want them to be deployed on all app servers in Stratos DC on a set schedule. Before that they need to test similar functionality with a sample cron job. Therefore, perform the steps below:

a. Install cronie package on all Nautilus app servers and start crond service.

b. Add a cron */5 * * * * echo hello > /tmp/cron_text for root user.

# Solution
As a root user in stapp01-
* 1  sudo yum install cronie
* 2  sudo systemctl status crond
* 3  sudo systemctl start crond
* 4  crontab -e (add "*/5 * * * * echo hello > /tmp/cron_text" to a line)
* 5  exit

repeat above for all app servers
