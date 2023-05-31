# MariaDB Troubleshooting
There is a critical issue going on with the Nautilus application in Stratos DC. The production support team identified that the application is unable to connect to the database. After digging into the issue, the team found that mariadb service is down on the database server.

Look into the issue and fix the same.

# Solution
As a root user enter the following commands.

* systemctl status mariadb.service -l
* mv /var/lib/mysqld/ /var/lib/mysql/
* systemctl start mariadb.service
* systemctl status mariadb.service

![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/8238785a-5078-4e78-83ae-b119730dfab7)
