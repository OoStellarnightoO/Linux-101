# Common shells
1. csh
2. zsh
3. tcsh

# Environment Variables
> printenv # by convention, environment var are uppercase
The PATH lists the directories where the shell will look for the command first
for example when you run 'ls' or 'python', it looks for these commands in the PATH
> export <var>=x #this sets a global variable 
> unset <var> #this unsets the var from PATH


When you open up a terminal, you are opening an Interactive Non-login shell
For example, like .bashrc

alias are custom shortcuts for code
for example
> alias del='rm -rfi'
> del #with the above alias set in .bashrc, typing del effectively runs rm -rfi
> source .bashrc #after changing settings in .bashrc, this reruns it


# Redirecting Input and Output
> ls /etc/ > <dest> #this outputs the content of ls /etc to a file. This overwrites
> ls /etc/ >> <dest> #this appends and does not overwrites
> find / -name 'sample.txt' 2> /dev/null #/dev/null is like black hole
> find / -name 'sample.txt' &> all.txt #this outputs the result but also returns the errors


# Pipes
Using pipes, we can connect stdin to stdout. '|' is a pipe. For example
> ls -l /etc/ | less 
> ls -l /etc/ | head -n 20 | tail -n 5 # this sends the output of /etc, extracts the first 20 lines and from there
extracts the last five lines


# Command History
> history | less #this returns commands that were previously ran
> !190 #this returns command 190 from the history
> !! #this runs the last command
> !cat #this runs the last cat command
> ^file1.txt^fileA.txt^ #this replaces the file that the last cmd was run on


# Command Substitution
> ls -l `cat file-list.txt` #a backtick will execute first
> 

