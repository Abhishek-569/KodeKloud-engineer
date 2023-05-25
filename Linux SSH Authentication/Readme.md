#Linux SSH Authentication
(Password-less ssh login)
The system admins team of xFusionCorp Industries has set up some scripts on jump host that run on regular intervals and perform operations on all app servers in Stratos Datacenter. To make these scripts work properly we need to make sure the thor user on jump host has password-less SSH access to all app servers through their respective sudo users (i.e tony for app server 1). Based on the requirements, perform the following:

Set up a password-less authentication from user thor on jump host to all app servers through their respective sudo users.
##Solution
On thor@jump_host:
1  ssh-keygen
2  ssh-copy-id -i ~/.ssh/id_rsa.pub tony@stapp01
3  ssh tony@stapp01
4  ssh-copy-id -i ~/.ssh/id_rsa.pub steve@stapp02
5  ssh steve@stapp02
6  ssh-copy-id -i ~/.ssh/id_rsa.pub banner@stapp03
7  ssh banner@stapp03
  
