# Working with Users and Groups
> who #return which user is currently logged in
> w #more details
> /etc/passwd #returns all users on the host

*/etc/passwd structure*
root:x:0:0:root:/root:/bin/bash
<username>:<used to store the hash>:<user unique ID>:<unique group ID>:<username>:<home directory>:<

- normal user accounts start with userid 1000 onwards

> cat /etc/group
- <group>:<used to store hash>:<grp ID>
- adm group is the administrator group while sudo grp is the list of users who can run sudo

> ls -la /home # reveal normal users' ownership of their home dir
> 

# File and Dir Permissions
> ls -la

<d/l/-><rwx><rwx><rwx>
<d/l/-> d stands for dir, l stands for link files and - is everything else
first <rwx> - rwx permissions for the owner
second <rwx> - rwx permissions for group users
third <rwx> - world rwx permissions

if a dir has no world x, you cannot run ls -la on that dir

> chmod 
Octo numbers for rws
r =4, w=2, x=1
> chmod 461 #sets owner to read only, set group to read and execute and world to execute only
> chgrp <group> <file> #change group ownership of file to new <group>
> 
# Changing Users and passwords
> sudo -u <user> <cmd> <file> #execute command as user on file
> su <user> #prompts password
> passwd #change passwd for current user
> sudo passwd <another user> 