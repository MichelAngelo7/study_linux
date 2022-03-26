# Topic 6:
### commands management users and groups


## useradd

create/add user in the system.

$useradd 'Name of User'  

## userdel 

Remove one user of system.


$userdel 'Name of User'

## usermod
Change the proprieties of one user.

$usermod -G 0 'Name of User'


$usermod -G root,bin,disk, 'Name of User'




## groupadd
Create/Add one group in the system.

$groupadd 'name'




## groupdel

Delete one group in the system.

$groupdel 'name'



## groupmod

Modify one group.

$groupmod -n 'new-name' 'old name'


## groups

List groups  of the group.

$groups 'user name'

## passwd
Define the password of the user.

$passwd 'user name'

## Files of configuration 

# /etc/passwd

content propriety of the user.

1       2     3       4    5   6                      7

user:x:1004:1004::/home/aluno:/bin/bash

1° Field = Login

2° Field = Password

3° Field = UID (User identifier)

4º Field = GID (Group Identifier)

5º Field = Comment

6º Field = Home Directory

7º Filed = Shell



## /etc/group

usermod -G 'group'  'user'

usermod -G 'group'  'root'

$tail -n 1 /etc/group

group:x :1005:aluno,root

1° Field =  Group name

2° Field = Group Password 

3° Field = GID (Group identifier)

4º Field = Users members of the group 

## /etc/shadow

aluno:!!:15438:0:99999:7::: -> User created after password defined

 aluno:$1$h1AA7S24$20fbYsUuUbYZyVAgOCZ6h1:15438:0:99999:7::: -> User created and password defined.



1° Field = Login

2° Field = Crypt Password

3° Field =   Last changed password

4º Field =  Minimum Password Age

5º Field =  Maximum Password Age

6º Field = Warn date of expiration 

7º Field = Inactive inform date of the expiration of the password

8° Field = Expire date of  automatic the account.  

## su

Change the current user to root user

$su

## sudo
permitted the current user execute one command has root user.

$sudo command. 

