# Topic 4:
### commands for system and hardware management.

## uname
Display information about the system, include the version of kernel 

$ uname -a 

## uptime 
display a summary of information about as:

current time;

time up of the system;

number of logged users; 

Load Average: display number of process in average waiting in row.
 need more information 
 
$uptime 
 
## free
Display information about use of memory RAM and SWAP

$ free -m

* -m display information in MB.

$free -s 10

wait 10 seconds and run again

## df
Display information about free use in disk.

$df -h

## du

Display information about size of directory or files

$du -hs /etc

## file

Display the type of a file.
  
$file < name of file >
 
 
## w

Display the output of the command uptime and information about users connected.

$w

## who
Display the users connected in the system.

$who

## whoami

Display the current user logged in the terminal. 

## dhclient
request IP address to server DHCP

$dhclient or dhclient < interface >

## ifconfig
Display current IP or configure IP for a given network adapter

$ifconfig < interface >

ifconfig < interface > [x.x.x.x] netmask [Y.Y.Y.Y]

## route
Displays or change routs or the default Gateway.

$ route add deafult gw [X.X.X.X]

$route -n

## ip
Displays and change network configurations, routing and tunneling.

$ip address or ip addr list or ip addr

define IP address to "enp0s3"

$ip address add x.x.x.x/mask dev < interface >

list the ip address of "enp0s3"

$ip address list enp0s3 or ip addr list enp0s3

show the routes
$ip route 

## dmesg

Display all hardware loaded of the system 

$dmesg

## lspci 

Show information of chipset and PCI devices 

$ lspci


## lsusb
Show information about USB devices connected on system.

$lsusb


## lsmod 
Show the modules loaded on system.

$lsmod

## insmod 

install modules in system 

$ insmod [file] < options >

## rmmod

remove modules on system 

$ rmmod < name of module >

## directory "/proc"

display information of the CPU

$cat /proc/cpuinfo

Display information of the IDE devices

$ls -l /proc/ide

Display information of the SCSI, SATA or SAS

$cat /proc/scsi/scsi

## fdisk
Display information of all storage devices connected on system and other functions.

$fdisk -l 
