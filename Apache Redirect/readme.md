# Apache Redirects

The Nautilus devops team got some requirements related to some Apache config changes. They need to setup some redirects for some URLs. There might be some more changes need to be done. Below you can find more details regarding that:

    httpd is already installed on app server 3. Configure Apache to listen on port 3002.

    Configure Apache to add some redirects as mentioned below:

    a.) Redirect http://stapp03.stratos.xfusioncorp.com:<Port>/ to http://www.stapp03.stratos.xfusioncorp.com:<Port>/ i.e non www to www. This must be a permanent redirect i.e 301

    b.) Redirect http://www.stapp03.stratos.xfusioncorp.com:<Port>/blog/ to http://www.stapp03.stratos.xfusioncorp.com:<Port>/news/. This must be a temporary redirect i.e 302.


# Solution
Run the folowing commands as `root` user.
* cat /etc/httpd/conf/httpd.conf |grep Listen
* vi /etc/httpd/conf/httpd.conf
* cat /etc/httpd/conf/httpd.conf |grep Listen(change the LISTEN to the required port)

![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/1ed55c0b-ddbd-4530-ab9b-974c23820081)

* vi /etc/httpd/conf.d/main.conf
* cat  /etc/httpd/conf.d/main.conf


![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/47604cf6-32ad-48b5-9e9b-c62af547570f)
* systemctl restart httpd
* systemctl status httpd
* curl http://stapp03.stratos.xfusioncorp.com:3002/
![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/c40f9578-b079-48cc-8a9a-c626790028ee)
* curl http://www.stapp03.stratos.xfusioncorp.com:3002/blog/
![image](https://github.com/Abhishek-569/KodeKloud-engineer/assets/64806938/f3978329-a2f4-4a4d-aff4-a9c98717a897)
