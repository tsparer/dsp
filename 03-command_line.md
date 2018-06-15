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

* pwd     = show current working directory or path
* ls      =  shows the files in the current directory
* ls -a   =  shows hidden files
* cd      = change directory
* mkdir   = creates a directory
* rmdir   = removes directory
* touch <filename> = creates a file
* rm      = removes file
* mv [options] <source> <destination>  = moves a file, can also be used to rename a file (by "moving it" to a new named space in the  same directory.
* cp <filename> <target_directory>  =  copy file : [here's nice list of commands and modifiers re: copy, remove, move etc.](https://www.hostingadvice.com/how-to/move-copy-delete-files-linux/)
* sed – search and replace within a file
* sort [-options] [path] – sorts contents of a file, alphabetically by default
* chmod [permissions] [path] = change permissions  [Specific permissions settings here](https://ryanstutorials.net/linuxtutorial/permissions.php) .  Often need to use when a script isn't running.
 * man = manual, look up commands etc. 
 * ./  - not really a command, but remember to include ./  before running a program from the command line.
 * Reminder on the distinction between [absolute and relative paths](https://ryanstutorials.net/linuxtutorial/navigation.php)
 
 

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

`ls`           displays a list of files  
`ls -a`        includes hidden directories (which begin with a dot)  
`ls -l`        list in long format (includes all sorts of additional information)  
`ls -lh`       list in long format, but use unit suffixes  
`ls -lah`      list all directories, including hidden ones, in long format, but use unit suffixes  
`ls -t`        sort by time modified (most recent first)  
`ls -Glp`      Colorize output, list in long-form, with a slash after each file name if the file is a directory  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > u  = display file access time  
> > R  = display subdirectories  
> > x  = display as rows across screen  
> > F  = flag filename  
> > c  = display timestamp  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs takes a command, and any related input, and executes it, possibly some number of times:  For example, to search for .txt files, you could use   
``` xargs find " \"*.txt" ``` ,  
or  
``` xargs -n 1 find "\*.txt"  "\*.png" ```  

The above code looks for all files with the extension .txt and then with the extension .png.  The option "n", and the argument "1" tell the xargs (and the function find) to except one argument per command line.  See [here](https://www.howtoforge.com/tutorial/linux-xargs-command/) for more.

 

