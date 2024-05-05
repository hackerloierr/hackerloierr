



On today's class
Further on User management
Linux File Ownership + Permissions
Software Installation
Script Installation
Package Installation Common errors


Some advanced user commands
To change password of user
sudo passwd username
To change user id
sudo usermod  -u new_id username
To Delete User
sudo userdel -r username 
To Change users on terminal
su - username


Sudoers file
The sudoers file is a file Linux and Unix administrators use to allocate system rights to system users
The user you created doesn’t have power to use sudo as the original one. 
This is Because it is not Added in the sudoers file ( የSudoዎች file )
To access this file
sudo visudo

Cont…
The 1st appearance when you open the sudoers file

Cont…
You can add the User you need to have access to the sudoers file, so he can use the sudo command.

Then after the user can use sudo command

Linux File permission
Every file on linux have their own
Owner 
Permissions
There is 5 main parts on the listing
Permission
Owners
Date
Size
filename

Ownership
Ownership is the owner of the file
This have 2 kinds
User
Group
To change the owner of file you can use the command 
chown user:group filename
	USER				GROUP

Permission
There are 3 types of permissions
Read ( r )
Write ( w )
Execute ( x )
The folders and files are differ with the ‘d’ and ‘-’ on the beginning of the permission.

Cont…
There still the permission have three parts.
user -group-other
User ( u ) => power of user defined on the the ownership
Group (g )=>  power of group defined on the the ownership
Other ( o ) =>  power of other users.
All ( a ) => power of all which can be found in the 3 above owners 
Command to change permission of file
chmod <option> filename
User             -group       -other

CHMOD command
This command helps to change file permission.
Those file permissions are read,write & execute.
Each of the permission have a number representations.
Read -> 4 -  r
Write -> 2 - w
Execute  -> 1 - x
Syntax
chmod <parameter> filename

Cont…
The parameter can be in numbers and symbols
Parameters in symbol
chmod a+x filename   ->  adding execute permission for all  ( chmod +x filename)
chmod u+x filename -> adding execute permission for user
chmod g+x filename -> adding execute permission for group
chmod o+x filename -> adding execute permission for other
chmod -x filename -> removing execute permission for all
chmod a+rwx , u-rw , g-x , o-xw filename -> gives rwx for all and removes something from all
B)	Parameters in Number
chmod 621 filename -> 6 for user, 2 for group, 1 for other  ( 6 = 4+2 ),  6 =r w
chmod 777 filename -> 7 for users, 7 for group , 7 for others (7 =4+2+1),  7 = rwx
Is giving the permission
Is taking / removing “   “

Breaktime
Create file called “Perm.txt” and give the following permission to it  
What is the equivalent of 631 permission in symbolic?
What is the equivalent of 200 permission  in symbolic?
What is the  numeric equivalent of 
Create a user called gtst & test with password 123456
Change the file user owner of Perm.txt to gtst and the group owner to root
Change the user password of gtst to “pass123”
Change the user id of ‘gtst’ to 1923
 Delete the user ‘test’
20 min

Special File Permissions	
There are another 3 special permissions, you may encounter on your pentest Journey.
They are
SUID bits(s) - set user ID bit - add 4 infront of our numeric value  ->    4000
SGID bits(S) - set group ID bit - add 2 infront of our numeric value ->  2777
Sticky bits(t) - set other ID bit - add 1 in front of our numeric value -> 1602
They are permissions like the execute(x), but they will set the execute permission to the user who settled them.
Example: if mr.A add suid bit to a program that program will be executed with permission of mr.A
Meaning if admin add suid bit on some program. Then any user if they got that program they can run it as root with any sudo password

Package installation on linux
ON linux to install softwares you use package managers.
Ex: apt,pacman,pkg,...
We will use debian package manager.
On debian the package manager i called ‘APT’ also there is called ‘dpkg’
Package managers are a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions.


The repository
This is the site/ server kali use to upload the packages

Advanced package tool / apt /
Apt is a free-software user interface that work with an online server to handle the installation and removal of software on Debian, and Debian-based Linux distributions.used for online and offline purpose.
The old ‘apt’ used as ‘apt-get’
Syntax
sudo apt update 
sudo apt search <softwarename>
sudo apt install <softwarename>
sudo apt remove <softwarename>
sudo apt upgrade 
sudo apt purge <softwarename>

Package dependencies 
A software can be built based on another program called ‘modules’
SO, a program to work properly, the dependencies have to be installed successfully. 
Those package managers install the software+dependencies.

example:

Dpkg / Debian package manager /
Dpkg is an offline package managing program.
Packages on debian have an extension “.deb”
Syntax
sudo dpkg -i <packagename>
sudo dpkg -r <packagename>
sudo dpkg -P <packagename>

Let’s get our hand dirty
Update your system repository
Search for package called ‘cmatrix’
Install ‘cmatrix’
Remove ‘cmatrix’
