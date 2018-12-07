# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> * show current working directory path: `pwd`  
> * creating a directory: `mkdir dir_name`
> * deleting a directory: `rm -d dir_name`
> * creating a file using `touch` command: `touch file_name`
> * deleting a file: `rm file_name`
> * renaming a file: `mv old_file_name new_file_name`
> * listing hidden files: `ls -a`
> * copying a file from one directory to another: `mv ./file_name ../other_dir/file_name`
> * show the size of a file: `du -h file_name`
> * view the manual entry for a command: `man command_name`
> * see where the executable file for a command is stored: `which command_name`
---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`

> `ls`: list files  
> `ls -a`: list all files (includes hidden files)  
> `ls -l`: list files with details (e.g. permissions)  
> `ls -lh`: list files with details; print file size in human readable format  
> `ls -lah`: list all files with details; print file size in human readable format  
> `ls -t`: list files sorted by time modified  
> `ls -Glp`: list files with details; distinguish directories with trailing slashes; color files by type  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> `-A`: list hidden files, but not `.` and `..`  
> `-R`: recursively list subdirectories  
> `-S`: sort by size  
> `-u`: sort by time of last access  
> `-P`: list symbolic links themselves instead of their referents  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> `xargs` takes a command name and a string of arguments and runs the command, providing it with those arguments. So it's an abstraction tool: you can give `xargs` what you want to do as data and it'll actually do the thing as if you were running the command directly.

> Example:
> ```Shell
> FILENAME="ship_manifest.txt"
> SEARCH_STRING="HMS"
> echo "$SEARCH_STRING $FILENAME" | xargs grep
> ```
