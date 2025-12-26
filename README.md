# DO1

## Part One
You Check the installed version of OS by running this command:
  *$ cat /etc/issue*
<img width="288" height="42" alt="{686C098B-F013-4126-8EC0-EDB913255092}" src="https://github.com/user-attachments/assets/e766e941-4f74-465f-aff7-5abb9afa560f" />

## Part Two
To create a new user and add into the group you should use this command:
  *$ sudo adduser <user_name>*
  *$ sudo usermod -aG adm <user_name>*
  *$ cat /etc/passwd | grep <user_name>*
<img width="770" height="361" alt="{C9C8D531-8475-4850-8735-846154F0FD69}" src="https://github.com/user-attachments/assets/41dc8e4d-058d-4a3a-8575-62f37e4b9a59" />

## Part Three
To set new machine name use this:
  *$ hostnamectl set-hostname <host_name>*

To show sys info including the current hostname use command:
  *$ hostnamectl*
<img width="426" height="206" alt="{FA4E4BA8-08C6-447F-B570-AFBA53C8DC52}" src="https://github.com/user-attachments/assets/98c35101-5d46-4f31-b12a-1d62215cb550" />


<img width="1920" height="1080" alt="{240AF51C-E279-478A-98E1-76ADF485B923} (2)" src="https://github.com/user-attachments/assets/64689a10-89b9-4b52-8921-7f748cf84953" />

You can set the timezone to your current location
  *$ sudo timedatectl*
  *$ sudo timedatectl set-timezone Asia/Tashkent*
  *$ sudo timedatectl*

<img width="809" height="344" alt="{DE468F43-9C3D-4599-903A-2DD17ACAC06B} (2)" src="https://github.com/user-attachments/assets/cab41c02-0cef-47d1-afd6-4babd97b0365" />

command output the names of the network interfaces:
  *$ ifconfig -a*

To get the IP address of the device you are working with from the DHCP server. Use this command:
  *$ hostname -I*

Defining the external IP address of the gateway:
  *$ curl ifconfig.me/ip*

Define the internal IP address of the gateway:
  *$ ip route show default | awk '/default/ {print $3}'*

<img width="1062" height="503" alt="{F9AF52AB-F69F-4C18-9EAE-43687D1D924C} (2)" src="https://github.com/user-attachments/assets/94ce5193-da36-430b-b52b-617a9609b285" />

Set static ip, gw, dns settings (use public DNS-servers such as 1.1.1.1 or 8.8.8.8).
  *$ sudo nano /etc/netplan/00-installer-config.yaml*
  
<img width="1269" height="247" alt="{FB137572-48D1-40C9-9A30-3B61290B13F5} (2)" src="https://github.com/user-attachments/assets/64712505-45cf-45e7-886e-f1e5873e3f58" />

Save the changes and reboot the machine
  *$ sudo netplan apply*
  *$ reboot*

Now make sure that the settings have been changed
  *$ ifconfig*

Also check if remote hosts 1.1.1.1 and 8.8.8.8 are pinged successfully
  *$ ping 1.1.1.1*
  *$ ping 8.8.8.8*

<img width="1017" height="830" alt="{1C95201E-EA14-4928-A00E-E73BE3A39B08} (2)" src="https://github.com/user-attachments/assets/dec6c4e5-abbb-4ef3-bd03-39d0ae8181c7" />

  
## Part Four
To update, simply type a command into the terminal. After updating the system packages,
if you enter the update command again, you should get a message that there are no updates.
  *$ sudo apt update*
  *$ sudo apt upgrade*
<img width="1375" height="305" alt="{5FADBE98-7F36-4309-9E75-E109CB04CE82} (2)" src="https://github.com/user-attachments/assets/d00a6539-187b-4a1d-bd6c-1c06aef08bcb" />

  

# Part Five
The command sudo is short for "Superuser Do". It is used in Unix operating systems and Unix-like systems
such as Linux to allow normal users to execute commands with elevated privileges or as a superuser
To allow a user to run a sudo command, you need these commands:
  *$ sudo usermod -a -G sudo user-1*
  *$ su user-1*
  *$ cat /etc/hostname*
  *$ sudo hostname arvi*
  *$ su arvillal*
<img width="634" height="143" alt="{695F6458-D3F0-4AF0-8D95-2201E0190F60} (2)" src="https://github.com/user-attachments/assets/63dcda2f-aa81-473e-8d8e-4542e05974a1" />


## Part Six
  *$ sudo timedatectl*
  *$ timdatectl show*
<img width="738" height="324" alt="{57AB2CBD-9F30-47CF-82A1-4B79C621B771} (2)" src="https://github.com/user-attachments/assets/ef50f48e-6b4d-4f06-9e3a-72494b648c87" />
  
## Part Seven
To install the text editor VIM, NANO, JOE, you must enter the following commands:
  *$ sudo apt install vim*
  *$ sudo apt install nano*
  *$ sudo apt install joe*

  *$ vim test_vim.txt*
Edit mode - I
To exit mode - Esc
To save changes and exit - :wq!
<img width="738" height="324" alt="{57AB2CBD-9F30-47CF-82A1-4B79C621B771} (2)" src="https://github.com/user-attachments/assets/67768d56-de42-4182-bbbe-32a6d7c846f0" />


  *$ nano test_nano.txt*
<img width="1332" height="455" alt="{B2E2BABA-04AC-4E90-815B-5CC05C567EA9} (2)" src="https://github.com/user-attachments/assets/01e6064c-9a90-4472-a15a-1041f0903fa8" />

  *$ joe test_nano.txt*
<img width="835" height="280" alt="{E9446258-8CAE-4915-81CC-B28A91474527} (2)" src="https://github.com/user-attachments/assets/83e3fdba-32f0-4ce5-bfbe-2be5232cfe05" />

## Part Eight
You need to install SSH service
  *$ sudo apt-get install ssh*
To configure auto-start services at system startup. Enter:
  *$ sudo systemctl enable ssh*
  *$ systemctl status ssh*
<img width="1327" height="246" alt="{64885AC4-82A5-4BFB-A082-BF103D30D708} (2)" src="https://github.com/user-attachments/assets/123492a1-0d57-405d-938d-76f5c7056d9b" />

Reconfigure the SSHd service on port 2022
  *$ sudo nano /etc/ssh/sshd_config*
  *$ systemctl restart sshd*

<img width="982" height="1007" alt="{D5B25412-1571-4868-9D6C-706FB95A1FAB} (2)" src="https://github.com/user-attachments/assets/4386a7cf-5d36-45b7-af49-ce257944694c" />

To show the presence of the sshd process, using the ps command.
  *$ ps -e | grep sshd*
<img width="479" height="43" alt="{E20968F7-71EF-45F3-8B98-47C16DCFE03E} (2)" src="https://github.com/user-attachments/assets/ccdfea68-b242-4e4b-b483-a841a54f6721" />
  

## Part Nine
Top command output report from top:
  *$ top*
<img width="1887" height="1003" alt="{8C493E37-1AD4-4FD0-9074-5D7377D875CE} (2)" src="https://github.com/user-attachments/assets/60062501-63c2-43d0-8f90-9c4b8f2c1b87" />
uptime - 0 min
number of auth users - 1
total system load - 0,27 0,10 0,03
total number of processes - 128
cpu  load - 0,1
memory load - 1910/1967
PID of most memory proc- 1
PID of most CPU time - 727

### Screensohts of htop command output:
<img width="1909" height="1014" alt="{9FBB4AEA-B913-4270-BD91-C5B23393A3B0} (2)" src="https://github.com/user-attachments/assets/18e29c8a-c752-4d30-997e-5985c2828a25" />

SORT BY PID
<img width="1915" height="1008" alt="{47785148-12ED-4619-AB76-CCAA7251B792} (2)" src="https://github.com/user-attachments/assets/d9f1ce16-fb66-48e7-b3db-c27e2a0190d9" />

SORT BY PERCENT_CPU
<img width="1918" height="1005" alt="{446B4F59-9BF3-40FD-A73E-AEB6EFE5AE48} (2)" src="https://github.com/user-attachments/assets/4bdac2f6-44ab-49d5-9c81-23d6a13c350a" />


SORT BY PERCENT_MEM
<img width="1910" height="1006" alt="{3C8F0BCF-D11B-46D4-B7DF-4BB36DAEC6D2} (2)" src="https://github.com/user-attachments/assets/48406177-2980-4fcd-aba6-c5af330892c5" />


SORT BY TIME
<img width="1911" height="1005" alt="{46E88D3B-A55F-4497-BE1E-1D2131381A75} (2)" src="https://github.com/user-attachments/assets/1d20d714-d9a8-46a6-ba7e-3f4690426b75" />


FILTER 'sshd'
<img width="1919" height="313" alt="{7EE1ABFD-1210-4AE5-90D3-C069E3A66E15} (2)" src="https://github.com/user-attachments/assets/832b3d3b-124a-45fd-8783-d9837e452a8e" />


SEARCH 'syslog'
<img width="1916" height="1000" alt="{AFD84C96-358D-479A-B0F9-C4CB471A8E9E} (2)" src="https://github.com/user-attachments/assets/8d3f2bb9-dc8e-4af8-a752-ec89fc9721fb" />




Advanced hostname, clock and uptime output
<img width="2202" height="1648" alt="image_2025-12-15_00-24-08 (2)" src="https://github.com/user-attachments/assets/ddc5d1a5-e2b1-4cb8-9d27-a42d45833673" />

<img width="2200" height="1650" alt="image_2025-12-15_00-24-22 (2)" src="https://github.com/user-attachments/assets/67855dbf-4736-4d58-9140-0e2d76870ce2" />


## Part Ten
  *$ sudo fdisk -l
  $ swapon*
<img width="1113" height="494" alt="{3D3606E3-9654-4116-9A96-D76B6D97C8A2} (2)" src="https://github.com/user-attachments/assets/a6af677a-7f48-40b2-af7e-9130b3461e6c" />
HDD name - VBOX HARDDISK
HDD SIZE - 15GiB
Number of sectors - 27781120
Swap size - 1,8G

## Part Eleven
  *$ df*
<img width="1066" height="374" alt="{6FD4F298-990D-4735-A2F0-130660E00F83} (2)" src="https://github.com/user-attachments/assets/2d685146-2e05-4933-96ad-d0826931f515" />
Partion size - 10218772 Kbyte
Used space size - 4649560 Kbyte
Free space size - 5028540 Kbyte
Percent of usage - 49% Kbyte

## Part Twenty
  *$ sudo du -sh /var/log /var /home 
  $ sudo du -s --block-size=1 /var/log /var /home
  $ sudo du -sh /var/log/* 
<img width="838" height="786" alt="{679D1D59-6138-4DD8-B3F6-29F9CDA0FF22} (2)" src="https://github.com/user-attachments/assets/99f0f1ff-262f-47fc-98ac-58d69a0bff0f" />


## Part Thirty
  *$ ncdu /home/*
<img width="1032" height="233" alt="{8F873A3B-902C-49E5-832A-D1043666FFA4} (2)" src="https://github.com/user-attachments/assets/8ee71c59-2b86-4690-bffd-0950b46c091e" />

  *$ ncdu /var/*
<img width="935" height="406" alt="{F5C412A8-DEB5-4D22-9BA8-441B86DDC6BA} (2)" src="https://github.com/user-attachments/assets/fb7b0c92-7ffe-4958-8edc-6603d8a336fe" />

  *$ ncdu /var/log/*
<img width="952" height="607" alt="{C71886A7-9074-4B72-B3D7-8897208F9B6E} (2)" src="https://github.com/user-attachments/assets/8a00d605-5932-44d3-b9eb-dfb03916b4b3" />


## Part fourteen
  *$ sudo nano /var/log/dmesg
  $ sudo nano /var/log/syslog
  $ sudo nano /var/log/auth.log*
  $ sudo systemctl restart ssh
  $ cat /var/log/syslog*
<img width="1895" height="1009" alt="{2BEC6926-BD13-413E-8C6C-1BF6B46F9E83} (2)" src="https://github.com/user-attachments/assets/40fdb9bd-72c0-41aa-a7b1-32026aa2fb3d" />
<img width="1917" height="1005" alt="{A52F616B-E605-41CB-81AF-DF43A0F29332} (2)" src="https://github.com/user-attachments/assets/50248509-3ea6-4a57-aeeb-993da1be1081" />
<img width="1914" height="1011" alt="{A5E09B4D-3E88-4052-804D-2AB75EF9F1DB} (2)" src="https://github.com/user-attachments/assets/ff80bdc5-4ebb-4f80-810c-5e2c935fcbea" />
    Last successful authorization: Dec 15 23:58:53;
    Username: arvillal;
    Login method: pam-unix.


## Part Fifteen
To through the job scheduler, run the uptime command every 2 minutes.
You need to open the scheduler and add a task (*/2 * * * * uptime).
  *% sudo crontab -e*
<img width="1994" height="766" alt="image_2025-12-15_00-30-05 (2)" src="https://github.com/user-attachments/assets/4da78c58-114e-479b-8d26-fdf58e03e0f9" />

  *% sudo crontab -l*
<img width="1375" height="936" alt="{65331F12-2FD5-42CE-9A00-212B29EAF396}" src="https://github.com/user-attachments/assets/3e86a43f-a69e-4fc3-bb03-050461ac1d70" />

Deleting all tasks from the scheduler:
  *$ sudo crtontab -r
  $ sudo crtontab -l*
<img width="412" height="103" alt="{3B4CFDE9-B1CA-46A4-962A-89178854A222} (2)" src="https://github.com/user-attachments/assets/f1a377ac-648f-49dc-a70a-3a9e12c7e5a9" />










