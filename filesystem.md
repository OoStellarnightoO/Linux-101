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
> 

# Text Files
>head word.txt #returns first 10 lines
>head -n 5 word.txt #returns first five lines
>tail word.txt #returns last ten lines, useful to checks for updated logs
>diff <txt1> <txt2> #returns the differences between both files
>

# Spaces in paths and filenames
to deal with spaces:
you can use\ to escape spaces
'my dir.txt' == my\ dir.txt

Wildcard usage
> ls file*.txt #this returns any .txt file with file inside the name
> ls file?.txt #this only returns files that are file{x} where x is any alphanum
> ls **/*.txt 
> ls file[123].txt # only return file1 or file2 or file3
> ls file[a-zA-Z].txt #only return file{a} where a is between a or z
> 


#Hard and Soft filesystem links
- Kind of like shortcuts in Windows thought it is more
- A pointer/reference to a file at another location
- by default, a hard link is created. when the file is deleted, the file 
- continues to work as long as the hard link exits
>ln <file1> <file2> #hardlink file1 to file2
- editing file1 will reflect the changes to file2

**Creating hard links to dirs may cause problems!**

>lin -s <file1> <file2> #creates a soft link
- Unlike hard links, soft links "break" if file1 moves or deleted
- Soft links are better for dirs


# Compressing and Archiving Files
> zip <zipfile> <file> <file1> <file2> #adds file,file1 and file2 to zipfile
> unzip <zipfile> -l <dest> #unzips zip file into dest
> unzip -r <zipfile> dir1 dir2 #unzips recursively into dir1 and dir2
> tar cvf <tarfile> file?.txt dir? shake.txt 
#the above command creates a tar file combining all file?, all dir and shake.txt


# Searching the filesystem
> find . -name 'file*.txt' # searches in current dir for file*.txt
> find . -iname 'file*.txt' # non-case sensitive
> locate <file> # searches the entire file system
> which <cmd> # returns the path of the command