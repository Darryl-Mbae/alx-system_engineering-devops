0-current_working_directory - "pwd" prints the absolute path name of the current working directory.

1-listit - "ls" Display the contents list of your current directory.

2-bring_me_home - "cd" Write a script that changes the working directory to the user’s home directory. You are not allowed to use any shell variables

3-listfiles - "ls - l" Display current directory contents in a long format

4-listmorefiles - "ls -la" Display current directory contents, including hidden files (starting with .). Use the long format.

5-listfilesdigitonly - "ls -lna" Displays current directory contents. Long format with user and group IDs displayed numerically And hidden files (starting with .)

6-firstdirectory - "mkdir /tmp/6-firstdirectory" Creates a script that creates a directory named holberton in the /tmp/ directory.

7-movethatfile - "mv /tmp/betty /tmp/my_first_directory/" Moves the file betty from /tmp/ to /tmp/my_first_directory

8-firstdelete - "rm /tmp/my_first_directory/betty" Deletes the file betty. The file betty is in /tmp/my_first_directory

9-firstdirdeletion - "rm -r /tmp/my_first_directory" Deletes the directory holberton that is in the /tmp directory.

10-back - "cd -" Write a script that changes the working directory to the previous one.

11-lists - "ls -la . .. /boot" Writes a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.

12-file_type - "file /tmp/iamafile" Writes a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script.

13-symbolic_link - "ln -s /bin/ls __ls__" Creates a symbolic link to /bin/ls, named ls. The symbolic link should be created in the current working directory.

14-copy_html - "cp -u *.html .." Creates a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory. You can consider that all HTML files have the extension .html

15-lets_move - "mv [[:upper:]]* /tmp/u" Creates a script that moves all files beginning with an uppercase letter to the directory /tmp/u. You can assume that the directory /tmp/u will exist when we will run your script

16-clean_emacs - "rm *~" Creates a script that deletes all files in the current working directory that end with the character ~.

17-tree - "mkdir -p welcome/to/school" Creates a script that creates the directories welcome/, welcome/to/ and welcome/to/holberton in the current directory. You are only allowed to use two spaces in your script, not more.

18-commas - "ls -xamp" Writes a command that lists all the files and directories of the current directory, separated by commas (,)

19 - vi school.mgc
then type in the code below
```
0 string SCHOOL School data
!:mime School
```
exit vi 
then type in the comman  "file -C -m school.mgc"
