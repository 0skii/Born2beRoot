# Born2beRoot
System Administration

<div align="center">
On this project, I learned how to create and setup a virtual machine manually using a Debian operating system. I had to recreate a specific pattern of partitions (included encrypted ones) using LVM. Similar to this image:

![image](https://user-images.githubusercontent.com/117108505/226703029-a097c1b1-b75e-46b0-9a10-6f09ace6ecfc.png)

Once I had a working nongraphic machine, I set up a heavy password policy for new users. Implementing these requirements:
  
![pw quality](https://user-images.githubusercontent.com/117108505/226710487-f69014e3-a64e-4af2-8312-4f4140eadf7a.png)

Next, I learned about SSH and UFW (Secure Shell and Uncomplicated Firewall), how ports work and how to setup UFW rules enabling me to connect to my VM from the hosting machine for example. Just like this:

![ssh](https://user-images.githubusercontent.com/117108505/226903258-e4fb1d95-c518-4fc4-8386-e23e2d9fbd2f.png)

![ufw](https://user-images.githubusercontent.com/117108505/226903316-bc2cb726-85cb-4db8-91f0-1f9f8595cf81.png)

After that, I had to modify some sudo rules for security reasons. Securing some paths, implementing a sudo logfile, limiting password tries and some other things. I also gave sudo level permissions to my user. Which you can see here:

![visudo](https://user-images.githubusercontent.com/117108505/226904581-f53fe75e-3079-41eb-be0e-4aa37611146f.png)

The "monitoring.sh" is a bash script file that only my user can access if forgetting my password would occur for example, or other reasons.

![monitoring script](https://user-images.githubusercontent.com/117108505/226906795-bd995aa3-02bb-40ba-9aa3-c2b265c95082.png)

I also had to make it run every 10 minutes from when the machine booted, so I learned how to use crontab. I set it up like this:
  
![crontab](https://user-images.githubusercontent.com/117108505/226905507-83e2ca21-6038-4b3f-8c8e-59d16a49a677.png)

Adding to this I implemented a cronjob that made the first task sleep for 10 seconds so when I reboot my machine the script wouldn't appear before i logged into it.
