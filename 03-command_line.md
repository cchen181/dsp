# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

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

> > 'pwd' shows current working directory path ('print working directory')
* 'ls' lists files and directories within the current folder
* 'cd' change directory. It switches you into the directory you specify
* 'cd ..' moves you up a directory
* 'mkdir' creates a directory ('make directory')
* 'touch file.txt' creates a file.txt file using the 'touch' command
* 'cp directory/file.txt newdirectory/' copies file.txt from directory to newdirectory (i.e. copying a file from one directory to another)
* 'ls -a' lists hidden files and folders in current directory
* 'mv file.txt newfilename.txt' renames a file (renames file.txt to newfilename.txt)
* 'rm file.txt' deletes a file ('remove' file.txt)
* 'rm -r directory/' deletes a directory ('remove recursively', which deletes a directory and all its child directories)

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

> > 'ls' lists files and directories within the current folder
* 'ls -a' lists files and directories, *both hidden and not hidden*, within the current folder
* 'ls -l' lists files and directories *in a long format* within the current folder
* 'ls -lh' lists files and directories *in a long human-readable format* within the current folder
* 'ls -lah' lists files and directories *both hidden and not hidden, in a long human-readable format* within the current folder
* 'ls -t' lists files and directories *by time last modified* within the current folder
* 'ls -Glp' lists files and directories *in a long format, without group names, with slashes following directory names* within the current folder
---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > My top 5 ls options on that list are -a, -d, -l, -t, and -u.

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > 'xargs' enables the execution of command lines from standard input. A use case is 'find Downloads/ *.pdf | xargs rm -rf '

 

