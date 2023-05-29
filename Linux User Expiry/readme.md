# Linux User Expiry
A developer john has been assigned Nautilus project temporarily as a backup resource. As a temporary resource for this project, we need a temporary user for john. It’s a good idea to create a user with a set expiration date so that the user won't be able to access servers beyond that point.

Therefore, create a user named `john` on the App Server 1. Set expiry date to `2021-04-15` in Stratos Datacenter. Make sure the user is created as per standard and is in lowercase.


# Solution

As a root user enter the following commands.  
* 1  useradd john
* 2  chage -l john
* 3  usermod -e 2021-04-15 john 
* 4  chage -l john
  
### Before the account expiry is set.
![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/e92d64e5-4053-4030-be7b-a89806f6360e)

### After the account expiry is set.
![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/dbfdbe7d-4493-434b-9a00-03c7530dc271)
