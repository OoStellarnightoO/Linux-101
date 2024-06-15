# Linux Filesystem Hierarchy Standard
> / #root directory
> /bin #executable programs needed in single user mode
> /boot #static files for boot loader
> /dev #special or device files
> /etc #configuration files local to the machine
> /lib 
> /media #mount points for removable media
> /mnt #also a mount point
> /proc #mount point for the proc filesystem
> /tmp 
>

# Devices, Partitions and Mounting
hardrive identifiers:
> for example /dev/sda stands for sata-drive, 'a' stands for the first drive
> hard drives may be partitioned; for example, /dev/sda1, /dev/sda2
> /etc/fstab #this gives information on the partitions
> mount #this shows current mounted drives
> df -h #this returns the storage space on the mounts
> 

# Absolute and Relative Paths
> ./ #this stands for current working directory
> ../ #this stands for the parent directory of the current dir


# Working with Files and Dirs
> ls -l <file> #this returns the last modification time
> touch <file> #this will update ht mod time
> touch <file> #if file does not exist, it creates a blank file
> cp <file> <destination> #copy and paste to dest
> mv <file> <dest> #moves the file, can also be used to rename the file
> rm <file> #deletes the file, -r deletes recursively
> mkdir <name> #creates directories
> rmdir <dir> # removes empty dir, -r to delete recursively


# Spaces in paths and filenames
to deal with spaces:
you can use\ to escape spaces
'my dir.txt' == my\ dir.txt

