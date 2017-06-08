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

> > 
pwd (show current working directory path)
mkdir DIR_NAME (creating a directory)
rm -r DIR_NAME (deleting a directory)
touch FILE_NAME (creating a file using `touch` command)
rm FILE_NAME (deleting a file)
mv OLD_FILNAME NEW_FILNAME (renaming a file)
ls -a (listing hidden files)
cp OLD_DIR/FILE_NAME NEW_DIR/ (copying a file from one directory to another)
cat FILE_NAME (display contents of file in terminal)
> (redirection)
grep string FILE_NAME (search for instance of pattern and return the result)
sed "s/find_string/replace_with_string/g" FILE_NAME (find and replace all instances of a string within a file)
| (piping - pipe the output of command on the left as an input for the command on the right)


---

### Q2.  List Files in Unix   

What do the following commands do:  

> > 
`ls`  - list the contents of a directory
`ls -a`  - list all contents of a directory including hidden files
`ls -l`  - list the contents of a directory in long format (including permissions, size, last modified, etc.)
`ls -lh`  - list the contents of dir in long format with size in human readable format(KB,MB,GB)
`ls -lah`  - list all the contents of dir (including hidden files) in long format with size in human readable format(KB,MB,GB)
`ls -t`  - list contents of dir in order of modified time from newest to oldest
`ls -Glp`  - list dir contents in long format, omit the Group column, mark directories with a forward slash



---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > ls -R (for a nice macro-level view: provides listing of all children directories, sub-directories, sub-sub directories, et al.)
> > ls -S (sort by file size)
> > ls -1 (print each file or directory on a separate line)
> > ls -ltr (sort by last modified oldest to newest)
> > ls -X (sort alphabetically by entry extention)

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > xargs converts STDIN into an argument
**Example:**
*Say you wanted to remove from the working directory a list of files that are listed in a text file named old_files.txt*
cat old_files.txt | rm  *(<-- this command would not work)*
cat old_files.txt | xargs rm *(<-- this command would probably work)*
The reason for this is because piping feeds the results on the right as a STDIN to the command on the right. rm doesn't expect STDIN, it expects arguments. xargs remedies that by converting the contents of old_files.txt from STDIN to arguments.
 

