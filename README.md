# Linux
VmTutes Linux
Linux/Unix Index:
=================
0. Operating System
1. Introduction To Linux/Unix
2. Installation Red Hat Enterprice Linux
3. Terminal Overview
4. Filesystem Hierarchy 
5. Basic Commands
6. VIM Editor
7. Hard link
8. File Permissions
9. Package/Soft Management 
10. User and Group Administration
11. Login with custom user


WHAT IS OPERATING SYSTEM?
=========================
Operating system is an interface between user and the computer hardware. The hardware of
the computer cannot understand the human readable language as it works on binaries i.e. 0's
and 1's. Also it is very tough for humans to understand the binary language, in such case we
need an interface which can translate human language to hardware and vice-versa for effective
communication.

TYPES OF OPERATING SYSTEM:-
===========================
Single User - Single Tasking Operating System
Single User - Multitasking Operating System
Multi User - Multitasking Operating System

SINGLE USER - SINGLE TASKING OPERATING SYSTEM
---------------------------------------------
In this type of operating system only one user can log into system and can perform only one
task at a time.
E.g.: MS-DOS

SINGLE USER - MULTI TASKING OPERATING SYSTEM
--------------------------------------------
This type of O/S supports only one user to log into the system but a user can perform multiple
tasks at a time, browsing internet while playing songs etc.
E.g.: Windows 98

MULTI USER - MULTI TASKING OPERATING SYSTEM
-------------------------------------------
This type of O/S provides multiple users to log into the system and also each user can perform
various tasks at a time. In a broader term multiple users can logged in to system and share the
resources of the system at the same time.
E.g.: UNIX, LINUX etc.

HISTORY OF UNIX
===============

Unix:- 
  > Orginally spelled UNICS(Uniplexed Information Computing System) 

In the beginning, there was AT&T.
Bell Labs’ Ken Thompson developed UNIX in 1969 so he could play games on a scavenged DEC
PDP-7. With the help of Dennis Ritchie, the inventor of the “C” programing language, Ken
rewrote UNIX entirely in “C” so that it could be used on different computers. In 1974, the OS
was licensed to universities for educational purposes. Over the years, hundreds of people
added and improved upon the system, and it spread into the commercial world. Dozens of
different UNIX “flavors” appeared, each with unique qualities, yet still having enough
similarities to the original AT&T version. All of the “flavors” were based on either AT&T’s
System V or Berkeley System Distribution (BSD) UNIX, or a hybrid of both.

During the late 1980’s there were several of commercial implementations of UNIX:

* Apple Computer’s A/UX
* AT&T’s System V Release 3
* Digital Equipment Corporation’s Ultrix and OSF/1 (renamed to DEC UNIX)
* Hewlett Packard’s HP-UX
* IBM’s AIX
* Lynx’s Real-Time UNIX
* NeXT’s NeXTStep
* Santa Cruz Operation’s SCO UNIX
* Silicon Graphics’ IRIX
* SUN Microsystems’ SUN OS and Solaris and dozens more.


LINUX/LINUS:-
==============
Linux was developed in 1991 by "Linus Torvalds" and a band of programmers who voluntarily
developed the core program of the system, the kernel. That program was originally compatible
for another operating system called Minix, but later development made it usable with GNU
software.

WHY LINUX?
==========
Fresh implementation of UNIX APIs
Open source development model
Supports wide variety of hardware
Supports many networking protocols and Configurations
Fully supported

Linux is a UNIX like OS:-
------------------------
Linux is a similar to UNIX as the various UNIX versions are to each other.
Multi-User and Multi-tasking: Linux is a multi-user and multi-tasking operating system. That
means that more than one person can be logged on to the same Linux computer at the same
time. The same user could even be logged into their account from two or more terminals at the
same time; Linux is also Multi-Tasking. A user can have more than one program executing at the
same time.

Wide hardware support: Red Hat Linux support most pieces modern x86 compatible PC
hardware.

Fully Supported: Red Hat Linux is a fully supported distribution Red Hat Inc. provides many
support programs for the smallest to the largest companies.

Installation
============

      -	Virtualization
        --------------
         Virtualization is the process of running a virtual instance of a computer system in a layer abstracted from the actual hardware. 
      	  Most commonly, it refers to running multiple operating systems on a computer system simultaneously. ..

      - Hypervisers
        -----------
         1. VMWare Workstation
         2. Virtual Box (Oracle Product)

      - Software
        --------
         1. Redhat Enterprice Linux 6.4
         2. Redhat Enterprice Linux 7.6 

Terminal Overview
=================

	Users
        -----
	Root user:- Root user will have administrater level access
	Normal user:- limited previlages
	   <Note:- as a devops engineer we will work in normal user)

	# Root user  Home Directory ~    /root
                     Root Directory /    /
 

	$ Normal User  Home Directory ~    /home/VmTutes
                       Root Directory /    /


Linux uses single rooted, inverted tree like file system hierarchy
                                             ---------------------      


/
It is parent directory for all other directories It is called as ROOT directory. It is represented by
forward slash (/) C:\ of windows

/root
It is home directory for root user (super user) It provides working environment for root user
/root is similar to c:\documents and settings\administrator

/home/ec2-user
It is home directory for normal users. It provide working environment.
/home is similar to c:\documents and settings\username

/boot
It contains bootable files for Linux, like vmlinuz (kernel)..... ntoskrnl Initrd (INITial Ram Disk) and
GRUB (GRand Unified Boot loader).... boot.ini, ntldr

/etc
It contains all configuration files like /etc/passwd - User info, /etc/resolv.conf -Preferred DNS,
/etc/dhcpd.conf - DHCP server
/etc is similar to c:\windows\system32\drivers\

/usr
By default soft wares are installed in /usr directory (UNIX Sharable Resources)
/usr is similar to C:\Program Files

/opt
It is optional directory for /usr. It contains third party softwares
/opt is similar to c:\Program FIles

/bin
It contains commands used by all users (Binary files)

/sbin
It contains commands used by only Super User (root) (Super user's binary files)

/dev
It contains device files, like /dev/had - for hard drives, /dev/cd rom - for cd drives
/dev similar to device manager of Windows

/proc
It contain process files, the contents are not permanent, they keep changing It is also called as
Virtual Directory. Its file contain useful information used by OS like
/proc/meminfo ... information of RAM/SWAP
/proc/cpuinfo ... information of CPU

/var
It contains variable data like mails, log files
/mnt

It is default mount point for any partition It is empty by default
/media

It contains all of removable media like CD-ROM, pen drive
/lib

It contains library files which are used by OS. Library files in Linux are SO (shared object) files
/lib is similar to .dll files of windows

Basic Commands
==============

ls (List)
---------
ls -l
ll
ls -alh

su (switch user)
----------------
su VmTutes(normal user)
su root
su - root
(Note:- wsitching from one user to other)

cd (change directory)
---------------------
cd VmTutes
cd ~

cat
---
cat > VmTutes (to create file)
cat VmTutes (to open a file) 
cat >> VmTutes (appending)
cat -n VmTutes

touch
-----
touch tek1 tek2 tek3
(Note:- to create multiple empty file at a time)

tee
---
tee a1 a2
(Note:- to insert same input to multiple file)

rm
--
rm <file_name>
rm VmTutes
rm -f VmTutes (forcefully)

mkdir(make directory)
---------------------
mkdir <folder_name>
mkdir VmTutes

copy
----
cp <source> <destination>
cp <file_name> <folder_name>
cp <file_name> <file_name> (cp: overwrite `VmTutes'?)
cp -r <folder> <folder>
cp VmTutes.txt  devops/alpha.txt
cp a*  <destination>

mv
--  
mv <source>  <destination> 
mv tek  VmTutes
mv <folder_name> <folder_name>

rename
------
mv <old-name>  <new-name>
mv tek VmTutes
(Note:- 1. if you already have a file with name VmTutes then it will overwrite? 
        2. if you already hava a folder with name VmTutes then it will move the file to VmTutes folder
        3. mv: overwrite `VmTutes'?)

append ('>>')
-------------
echo "welcome to VmTutes online training" >> tek  (single line appending)
echo "welcome to VmTutes online training
      welcome to VmTutes online training
      welcome to VmTutes online training" >> tek  (multy line appending)
cat >> VmTutes 
welcome to VmTutes online training
welcome to VmTutes online training
welcome to VmTutes online training
control + c(gracefull logout)

redirect ('>')
--------------
cat VmTutes > tek
(Note:- it will overwriten directly without any prompt message, in case the file name 'tek' already exists)

System Info
---------
date - show current date/time
uptime - show uptime
whoami - loggined in account
free - shows memory and swap usage
du
du -h/sh
df -h
VmTutes df

tar.gz
------
tar -xvf apache-maven-3.6.3-bin.tar.gz
tar -cvf apache-maven-3.6.3-bin
	eg:- tar -cvf apache-maven-3.6.3-bin.tar apache-maven-3.6.3-bin
tar -czvf apache-maven-3.6.3.tar.gz apache-maven-3.6.3
tar -xzvf apache-maven-3.6.3.tar.gz 

sort
----
sort <file_name> (alphabetical order)
sort -r(reverse) <file_name>
sort -h/-n(human-numeric-sort) <file_name>
sort -u(remove duplicates) <file_name>
sort <file-1> <file-2>
sort -u <file-1> <file-2> (two files sort and merge)
sort -rn VmTutes (big to small)

Hidden files
------------
ls -a  (to view hidden files)
touch/mkdir .VmTutes (to create hidden files/folders)
mv .VmTutes  VmTutes (un-hidden)
ls -d .*  (or) echo .*

Head && Tail
----    ----
syntax:-  head -n VmTutes.txt (it will prient default first 10 lines)

head -3 VmTutes.txt
tail -5 VmTutes.txt (last five lines in file)
head -15 VmTutes.txt | tail -9 (to prient specific lines in file)
head -20 VmTutes.txt | tail -1 (to print single line(20th line) in file)
head -9 VmTutes | tail -1 && head -16 VmTutes | tail -1 (specifing)
(OR)
cat VmTutes.txt | head -20  | tail -1
cat VmTutes.txt | head -7 | tail -5  
(OR)   
head -7 VmTutes.txt | tail -5

Pipeline( | )
-------------
def:- used to seperate the commands and to filter the exact data
     output from left side will pass it to right side as a input 

ls -l | grep VmTutes.txt
sort record.txt | uniq 
cat VmTutes.txt | head -7 | tail -5
cat VmTutes.txt | wc -l

wc(word count)
--------------
wc VmTutes
wc -l (lines)
wc -c/-m (char/byte count)
wc -L
wc -w (words)

find
----
Syntax:- find <where_to_search> <type> <file_name>

find /root -name sample.txt 
find / -type d -name VmTutes.txt
find . -type f -name "*.class"
find <.> <-name> <file-name>
find /root -inum 567890
find <folder_name> -user root
find /home -iname VmTutes.txt
find / -perm 777

sed
---
sed <s>/<old_name>/<new_name>/  <file_name>

sed 's/alphabet/VmTutes/g' <file_name>
       note:- "g" global replacement
sed 's/alphabet/VmTutes/' <file_name>
      note:- Here the “s” specifies the substitution operation. The “/” are delimiters. 
	     By default, the sed command replaces the first occurrence of the pattern in each line and it won’t replace the second, third…occurrence in the line. 
sed 's/alphabet/VmTutes/2' <file_name>
      note:- only replace second occurrence in a line
sed 's/alphabet/VmTutes/2g' <file_name>
      note:- g = global replacement
uname
-----
to see os-name
uname -a

shortcuts
=========

Ctrl + c --> gracefull logout
Ctrl + d --> exit/logout
Ctrl + Alt --> to Highlight the curser
Ctrl +ww  --> To switch between editors in vim. 
cd -   (like Ctrl + Z in windows)
cd .   (current directory)
cd ..  (one step back)
cd ../../../  (three steps back) 
cd devops/ --> meta char
q --> quit

hostname
--------
hostname is a combination of system name and DNS name.
localhost.localdomain (default)
hostname RedHat.DevOps.com
hostnamectl (this command for 6 version RHEL)
hostnamectl (this command for above 7 version RHEL)
hostnamectl set-hostname devops.VmTutes.com

awk
---
awk '{print $1}' VmTutes.txt
awk '{print $1,$4}' employee.txt
awk -F: '{print $1}' /etc/passwd

Cut
---
cut -d: -f1 /etc/passwd
cut -d" " -f1-f4 VmTutes.txt
cut -c -f1,f3 /etc/passwd
cut -c 1-5 /etc/passwd
cut -b 1- (all char till end of line)
cut -b -4 (before 4 char)
cut -d: -f1-4 /etc/passwd | head -5 | tail -1
cut -d: -f1-4 /etc/passwd | sed -n 10p

  

VI/VIM
======
VI Visual display editor
VIM Visual display editor improved

This is command mode editor for files. Other editors in Linux are emacs, gedit, nano..etc.
vi editor is most popular and flexible to use.

It has 3 modes:
1 Command Mode (default)
2 Insert mode (edit mode)
3 extended/colon command mode
Note: When you open the vim editor, it will be in the command mode by default.

	1. command mode
	---------------
	gg -To go to the beginning of the page
	G - To go to end of the page
	w - To move the cursor forward, word by word
	b - To move the cursor backward, word by word
	nw -To move the cursor forward to n words (5W)
	nb -To move the cursor backward to n words (5B)
	u - To undo last change (word)
	U - To undo the previous changes (entire line)
	Ctrl+R To redo the changes
	yy -To copy a line
	nyy - To copy n lines (5yy or 4yy)
	p - To paste line below the cursor position
	P - To paste line above the cursor position
	dw - To delete the word letter by letter (like Backspace)
	x - To delete the word letter by letter (like DEL Key)
	dd - To delete entire line
	ndd - To delete n no. of lines from cursor position(5dd)
	/ - To search a word in the file

	Insert Mode:
	------------
	i To begin insert mode at the cursor position
	A To Append at the end of the line
	o To insert a new line below the cursor position
	O To insert a new line above the cursor position

	3. Extended Mode: (Colon Mode)
	------------------------------
        Extended Mode is used for save and quit or save without quit using “Esc” Key with “:”

	Esc+:w To Save the changes
	Esc+:q To quit (Without saving)
	Esc+:wq To save and quit
	Esc+:w! To save forcefully
	Esc+:q! To quit forcefully
	Esc+wq! To save and quit forcefully
	Esc+:x To save and quit
	Esc+:20(n) To go to line no 20 or n
	Esc+: se nu To set the line numbers to the file
	Esc+:se nonu To Remove the set line number

	To open multiple files in vim editor
	# vi –o file1 file2
	# vi -O t1 t2
	To switch between files use Ctrl + ww

Hardlink/backup file
====================
ln file_name link_file_name(new)
ln tek VmTutes
Note:- to link with existing files we need to give -f 
  eg:- ln -f tek VmTutes

File Permissions:
=================

Permissions are applied on three levels
	@ Owner or User level
	@ Group level
	@ Others level

Access modes are of three types
	@ r read only
	@ w write/edit/delete/append
	@ x execute/run a command

Access modes are different on file and directory:
Permissions           Files 		                Directory
-----------	      ------   				----------
r 		 Open the file                   'ls' the contents of dir

w           Write, edit, append, delete file      Add/Del/Rename contents of dir

x          To run a command/shell script          To enter into dir using 'cd'


command to give permissions :-  chmod

Permission can be set on any file/dir by two methods:-
1 Symbolic method (ugo)
2 Absolute method (numbers)

	(1) Symbolic method (ugo)
		u = user
		g = group
		o = others

		r = read
		w = write
		e = execute
		
		+
		-
		=
	eg:- chmod u+w,o-x <file_name/folder_name>
	eg:- chmod ugo=wrx <file_name/folder_name>

	(2) Absolute method (numbers)
		Read = 4
		Write = 2
		Execute = 1
		------------
		Total = 7
		------------
	eg:- chmod 420 <file_name/folder_name>
	eg:- chmod 777(full permissions) <file_name/folder_name> 

Software/package Manager
========================
To manage the software in Linux, two utilities are used,
1. RPM – REDHAT PACKAGE MANAGER
2. YUM – YELLOWDOG UPDATER MODIFIED

Note:- if you running ec2 instance then refer below link (or) directly also we can use
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/add-repositories.html

	(1).RPM(default)
	-------
	   RPM is a package managing system (collection of tools to manage software packages). RPM is a powerful software management tool for installing, uninstalling, verifying, querying and updating software packages.
           RPM is a straight forward program to perform the above software management tasks.

           Drawbacks
	   ---------
		>> Lenghthy commands
		>> everytime we need to search for packages to install,update,and remove.
		>> not able to resolve the dependencies
           RPM Commands
	   ------------
		- rpm -ivh tree-2.7.9-5.el6.2.i686.rpm
		- rpm -q <package_name> (to check an installation)
		- rpm -qa (list all installed packages)
		- rpm -Uvh (to update)
		- rpm -evv (to erase) 
	
	 

	(2).YUM
	-------
		>> all the above rpm drawbacks overcomed here by configuring yum repo/server.

		step-1:- install vsftpd package with RPM (which you will get by default when install RHEL OS.)
		step-2:- Go to /var/ftp/pub/VmTutes (create folder in pub, mkdir VmTutes)
		step-3:- Go to /media/ and hit 'ls' command
		step-4:- cp -rvfp RHEL-6.4-x86_64*  /var/ftp/pub/VmTutes
		step-5:- Go to /etc/yum.repos.d  and creae file, vi VmTutes.repo and give below steps 
					-> [VmTutes]
					-> name=yumrepo
					-> baseurl=file:///var/ftp/pub/VmTutes
					-> enabled=1
					-> gpgcheck=0
		step-6:- yum clean all
		step-7:- yum list
		step-8:- yum repolist (optional)

	YUM Commands
	------------
        - sudo yum update -y
	- yum install <package_name>
	- yum remove httpd
	- yum update httpd
	- yum list all
	- yum list installed (it lists all installed packages)
	- yum list installed httpd (to check whether package is installed or not)


User and Group Administration
=============================
	
user
----
        In Linux/Unix user is one who uses the system. There can be at least one or more than
	one users in Linux at a time. Users on a system are identified by a username and a
	userid. The username is something that users would normally refer to, but as far as the
	operating system is concerned this is referred to using the user id (or uid). The
	username is typically a user friendly string, such as your name, whereas the user id is a
	number. The words username and userid are often (incorrectly) used interchangeably.
	The user id numbers should be unique (one number per user). If you had two usernames
	with the same user id, effectively there permissions would be the same and the files
	that they create would appear to have been created by the same user. This should not
	be allowed and the useradd command will not allow usernames to share the same
	userid.

	Some Important Points related to Users:
	* Users and groups are used to control access to files and resources
	* Users login to the system by supplying their username and password
	* Every file on the system is owned by a user and associated with a group
	* Every process has an owner and group affiliation, and can only access the resources its

	owner or group can access.
	* Every user of the system is assigned a unique user ID number ( the UID)
	* Users name and UID are stored in /etc/passwd
	* User’s password is stored in /etc/shadow in encrypted form.
	* Users are assigned a home directory and a program that is run when they login (Usually a shell)
	* Users cannot read, write or execute each other’s files without permission.

        Types of users In Linux and their attributes:
        ---------------------------------------------
 
	TYPE          EXAMPLE        USERID(UID)      GROUPID(GID)     HOME-DIRECTORY        SHELL
	Super User     Root             0                  0               /root            /bin/bash

	System User   ftp, ssh      1 to 999          1 to 999           /var/ftp          /sbin/nologin
	Normal User Visitor,ktuser  1000 to 100000    1000 to 100000     /home/user name    /bin/bash


	In Linux there are three types of users.
		1. Super user or root user
		   Super user or the root user is the most powerful user. He is the administrator user.

		2. System user
		   System users are the users created by the softwares or applications. For example if we
		   install Apache it will create a user apache. These kinds of users are known as system users.

		3. Normal user
		   Normal users are the users created by root user. They are normal users like Rahul,
		   Musab etc. Only the root user has the permission to create or remove a user.

	Whenever a user is created in Linux things created by default:-
	---------------------------------------------------------------
	* A home directory is created(/home/VmTutes)
	* A mail box is created(/var/spool/mail/VmTutes)
	* unique UID & GID are given to user
	* primary group


	There are two important files a user administrator should be aware of.
	----------------------------------------------------------------------
		1. "/etc/passwd"
		2. "/etc/shadow"
		Each of the above mentioned files have specific formats.

	1. /etc/passwd
	   root:x:0:0:comment:/home/devops/:/bin/bash
	   VmTutes:x:0:0:devops-engineer:/home/VmTutes/:/bin/bash

		The above fields are
		* root =name
		* VmTutes = normal user name
		* x= link to password file i.e. /etc/shadow
		* 0 or 1= UID (user id)
		* 0 or 1=GID (group id)
		* root or bin = comment (brief information about the user)
		* /root or /bin = home directory of the user
		* /bin/bash or /sbin/nologin = shell

	2. /etc/shadow
		root:$1fdsfsgsdfsdkffefje:14757:0:99999:7:::
		The above fields are

		* root = User name
		* $1fdsfsgsdfsdkffefje = Encrypted password
		* 14757 = Days since that password was last changed.
		* 0 = Days after which password must be changed.
		* 99999 = Days before password is to expire that user is warned.
		* 7 = Days after the password is expires that the user is disabled.
		
	Deleting a User:
	----------------
	* To delete a user the syntax used is
	* userdel <username> it will only delete the user but home directory will be there. To delete the user with its home directory use the following command.
	* userdel –r < user name >
	* userdel –r ktuser2

	The password parameters:
	------------------------
	* For any user we can set the parameters for the password, like min and max password age,
	  password expiration warnings and a/c expiration date etc.
	* To view the advanced parameters of the user, use

	* chage -l < user name>
	* chage -l VmTutes
	* Last password change: When the password was change last time.
	* Password expires: Password expiry date
	* Password inactive: After password expiry grace period before the account gets locked.
	* Account expires: Date on which the account expires.
	* Minimum number of days b/w password change: once the password is changed, it cannot be changed until a min period of specified date. [0] means never.
	* Max number of days b/w password change: After changing the password how long it willbe valid for.
	* Number of days of warning before password expires: start of warnings to change the password, no. of days before the password expires.

GROUP
-----
	* Users are assigned to groups with unique group ID numbers (the GID)
	* The group name and GID are stored in /etc/group
	* Each user is given their own private group
	* They can also be added to their groups to gain additional access
	* All users in a group can share files that belong to the group

		Each user is a member of at least one group, called a primary group. In addition, a user can be a
		member of an unlimited number of secondary groups. Group membership can be used to
		control the files that a user can read and edit. For example, if two users are working on the
		same project you might put them in the same group so they can edit a particular file that other users cannot access.

	- A user’s primary group is defined in the /etc/passwd file and Secondary groups are defined in the /etc/group file.
	- The primary group is important because files created by this user will inherit that group affiliation.

	- To create a group the syntax is
	- groupadd <name for the group>
	- groupadd VmTutes
	- gpasswd -a VmTutes tek (to add single user into group)
	- gpasswd -M t1,t2,t3 tek (to add multiple users into group)
	- gpasswd -d t1 tek (deleting user't1' from group tek)
	- groupdel <group_name>
      
           cat /etc/group


Login with custom user
======================
1. create user
     # useradd VmTutes
2. Generate Password for vmtutes
     # passwd VmTutes
3. add VmTutes user in "visudo" (or) /etc/sudoers file for sudo permissions
      # vmtutes ALL=(ALL) NOPASSWD: ALL
4. Enable "PasswordAuthentication yes" in vi /etc/ssh/sshd_config  file.
5. Restart the "sshd" service
     # systemctl restart sshd
Note:- ssh vmtutes@192.3.4.5



Job Schudles
==============
	In any operating system, it is possible to create jobs that you want to reoccur. This process,
	known as job scheduling, is usually done based on user-defined jobs. For Red Hat or any
	other Linux, this process is handled by the cron service or a daemon called crond, which can
	be used to schedule tasks (also called jobs). By default, Red Hat comes with a set of
	predefined jobs that occur on the system (hourly, daily, weekly, monthly, and with arbitrary
	periodicity). As an administrator, however, you can define your own jobs and allow your
	users to create them as well.

	Options 						Explanation
	-------							-----------
	* 				            Is treated as a wild card. Meaning any possible value.
	*/5 				Is treated as ever 5 minutes, hours, days, or months. Replacing the 5 with another numerical value will change this option.
	2,4,6                           Treated as an OR, so if placed in the hours, this could mean at 2, 4, or 6 o-clock.
	9-17 				Treats for any value between 9 and 17. So if placed in day of month this would be days 9 through 17. Or if put in hours it would be between 9 and 5.

	Syntax
	-------
        minutes      hours     days_in_month    months_in_year      days_in_week
	  30         4              2                12                  3
           *         *              *                 *                  *
	  */90       */3           */8                */3                */2
          *           22            20-25             1,4                6,7

	CRONTAB COMMANDS
	----------------
	Command 						Explanation
	-------							-----------
	crontab –e Edit your crontab file, or create one if it doesn’t already exist.
	crontab –l Display your crontab file.
	crontab –r Remove your crontab file.
	crontab -u If combined with –e, edit a particular user’s Crontab file 
	and if combined with –l, display a particular user’s crontab file. 
	If combined with –r, deletes a particular user’s Crontab file

errors and warnings
===================

	Virtualization
	--------------
	Go To Windows Security -->> Update and Security -->> Recovery -->> Advanced Setup --> Trouble shoot -->> Advanced Options -->> 
	UEFI Fireware Settings -->> restart -->> F10 -->> System Configuration (or) Security -->> Virtualization Technology -->> 
	press enter -->> Enable, Intel Virtualization Technology  -->> Press F10 to SAVE.

	Unsupported Hardware Detected
        -----------------------------
        Hit Enter button 
            (or)
        F12,esc,F11,F2 function key for next screen 


				                            ====THE END====       
			VmTutes, +91-7204143230(WhatsApp/Call), Email:- Vinodh-Machireddy@VmTutes.com
