### Change keyboard layout
loadkeys br-abnt2

### logout session
$ exit
$ logout
CTRL -D

### Shutdown System
$ shutdown -h now
$ init 0
$ halt
$ poweroff

### Reboot System
$ reboot
$ init 6
CTRL + ALT + DEL (reboot)

### FHS (File System Hietachy Standard)
/ - root of system
/boot - Files to start the system
/etc -  System configuration files and installed network services 
/bin -  Default commands of system for users 
/sbin - Default commands of system for root user
/var - logs of system and data of impression spool and cache
/root -  Directory of root user, system administrator 
/home -  Directory of users 
/dev -  Allows accesss to system devices
/lib - library share to programs and modules of kernel
/proc - System files kernel
/usr - file and data applications documents

  
 
commands: 

pwd 

show the current directory
$pwd

ls

list directory and files 
$ls

$ls -l list details information in columns 
$ls --color list directory and file with colors 
$ls -lh  human readable 


cd
change directory
$cd 

$cd - go to least directory 
$cd .. up one directory

passwd 
change password
$passwd

clear
clear the display
$clear or CRTL + L

move screen
shift + page up
or 
shift + page down

Help Commands
$man command
$command --help
$info command

cal
Calendar
$cal

date
show date and hour or update the informations 
$data  

alias
crate a alias of the commands 
$alias ls="ls --color"

mkdir
make directory
$mkdir "name"
$mkdir -p dir1/dir02/{network,linux,server} 
$mkdir dir{02,03,04}

rmdir 
remove directory
$rmdir "name"
$rmdir -rm "name" 

rm
remove files
$rm "name"
$rm -rf "name"	remove files and directory, not asked

Reverser search 
CTRL + R

tree
show the directory structure in form of tree
$tree name 

mv
move files or directory
mv "old patch" "new path or new name"

touch
create file text 
$touch "name"


cp 
copy files or directory
$cp  "old path" "new path or new name"
$cp -r used to copy directory 

ln
create link to file or directory
$ls -s "path or name" "path or name to destiny of link"

find
search to file os directory
$find -name "name"

du
disk usage show the size of files and directory
$du -hs * 



