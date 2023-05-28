# DNS Troubleshooting
You have to set Google DNS resolution in in your `stapp02` app server.

# Solution
 
 As a `root` user enter the following commands.
* 1  cat /etc/resolv.conf
* 2  echo nameserver 8.8.8.8 > /etc/resolv.conf
* 3  cat /etc/resolv.conf
* 4  echo nameserver 8.8.4.4 >> /etc/resolv.conf
* 5  cat /etc/resolv.conf


![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/1f8b5803-d88c-4904-9d72-30c1d3888db9)

