# Linux Collaborative Directories
The Nautilus team doesn't want its data to be accessed by any of the other groups/teams due to security reasons and want their data to be strictly accessed by the dbadmin group of the team.

Setup a collaborative directory /dbadmin/data on Nautilus App 1 server in Stratos Datacenter.

The directory should be group owned by the group dbadmin and the group should own the files inside the directory. The directory should be read/write/execute to the group owners, and others should not have any access.
# Solution
As a root user enter the following commands.

*  mkdir -p /dbadmin/data
* cd /dbadmin/
* chgrp -R dbadmin /dbadmin/data
* chmod g+rwx /dbadmin/data
* chmod o-rwx /dbadmin/data
* ls -al
* ll -lsd /dbadmin/data/


![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/4b1b3a63-8a67-4a7a-ba33-d7ce3bc0f75d)
