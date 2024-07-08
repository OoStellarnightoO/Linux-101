## Intro

When you open up a linux terminal, you'll see:

> bob@linux101:~$

*bob is the current user while linux101 is the machine's name*

*~$ indicates that you are a normal user. if .$, you are root*

### Useful starting commands
> whoami #returns user

> hostname #returns machine name

> pwd #print working directory

> ls -la #list all files (including hidden) in current directory

> cd #change directory

> man <command> #returns the manual for the <command>

> explainshell.com #a web app explaining commands 


### Command Line Arguments and Options


### Looking at Text Files
>more <wordlist.txt> #this prints out the content on the terminal

>less <wordlist.txt> #similiar to more but allows you to move up and down
    >/top #this searches for strings with top 

>cat <wordlist.txt> #takes the content of a file and output to console

>cat <file1> <file2> #concatenates files

>cat -b <file1> #outputs the content and number each line

>cat #without passing a file, this returns whatever we typed

*why use cat? it allows redirection. For example:*

>cat <file1> <file2> > <file3> # this concat file1 and file2 and outputs it to file3
