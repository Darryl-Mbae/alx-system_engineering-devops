# Shell Basics
Inside that directory, we can see its files and the pathway to its parent directory and the pathways to the subdirectories of the directory in which we are standing.
## pwd
The directory we are standing in is called the working directory. To see the name of the working directory, we use the pwd command.
```
[me@linuxbox me]$ pwd
/home/me
```
## ls
To list the files in the working directory, we use the ls command.
```
[me@linuxbox me]$ ls
Desktop    Downloads         foo.txt  Pictures  Templates
Documents  examples.desktop  Music    Public    Videos
```
| Command | Result |
|------|------------|
| ls /bin | List the files in the /bin directory (or any other directory we care to specify) |
| ls -l | List the files in the working directory in long format |
| ls -la | List all files (even ones with names beginning with a period character, which are normally hidden) in the parent of the working directory in long format |

A Closer Look at Long Format
If we use the -l option with ls, you will get a file listing that contains a wealth of information about the files being listed. Here's an example:

```

-rw-------   1 me       me            576 Apr 17  2019 weather.txt
drwxr-xr-x   6 me       me           1024 Oct  9  2019 web_page
-rw-rw-r--   1 me       me         276480 Feb 11 20:41 web_site.tar
-rw-------   1 me       me           5743 Dec 16  2018 xmas_file.txt

----------  -------    ------     ------- ------------ -------------
    |             |        |         |         |             |
    |             |        |         |         |         File Name
    |             |        |         |         |
    |             |        |         |         +---  Modification Time
    |             |        |         |
    |             |        |         +-------------   Size (in bytes)
    |             |        |
    |             |        +-----------------------        Group
    |             |
    |             +--------------------------------        Owner
    |
    +----------------------------------------------   File Permissions

```

## cd
To change the working directory we use the cd command. To do this, we type cd followed by the pathname of the desired working directory.
```
me@linuxbox me]$ cd /usr/bin
me@linuxbox bin]$ pwd
/usr/bin
```
## mv
The mv command moves or renames files and directories depending on how it is used.
| Command	| Results |
| ----------------- | --------------------------------|
| mv file1 file2	| If file2 does not exist, then file1 is renamed file2. If file2 exists, its contents are silently replaced with the contents of file1. |
| mv -i file1 file2 |	Like above however, since the "-i" (interactive) option is specified, if file2 exists, the user is prompted before it is overwritten with the contents of file1. |
| mv file1 file2 dir1	| The files file1 and file2 are moved to directory dir1. If dir1 does not exist, mv will exit with an error. |
| mv dir1 dir2	| If dir2 does not exist, then dir1 is renamed dir2. If dir2 exists, the directory dir1 is moved within directory dir2. |

## rm
The rm command removes (deletes) files and directories.
```[me@linuxbox me]$ rm file... ```
Using the recursive option (-r), rm can also be used to delete directories:
```[me@linuxbox me]$ rm -r directory...```
## mkdir
The mkdir command is used to create directories. To use it, you simply type:
```[me@linuxbox me]$ mkdir directory...```
## Wildcards
Using wildcards, it is possible to construct very sophisticated selection criteria for filenames. Here are some examples of patterns and what they match:


Pattern	Matches
| Patterns | Matches |
| -- | -----|
| *	| All filenames |
| g*	| All filenames that begin with the character "g" |
| b*.txt	| All filenames that begin with the character "b" and end with the characters ".txt" |
| Data???	| Any filename that begins with the characters "Data" followed by exactly 3 more characters |
| [abc]*	| Any filename that begins with "a" or "b" or "c" followed by any other characters |
| [[:upper:]]* | Any filename that begins with an uppercase letter. This is an example of a character class. |
| BACKUP.[[:digit:]][[:digit:]]	| Another example of character classes. This pattern matches any filename that begins with the characters "BACKUP." followed by exactly two numerals. |
| *[![:lower:]] 	| Any filename that does not end with a lowercase letter. |

## less
less is a program that lets us view text files.

## file
As we wander around our Linux system, it is helpful to determine what kind of data a file contains before we try to view it. This is where the file command comes in. file will examine a file and tell us what kind of file it is.

To use the file program, we just type:

```file name_of_file```

## man
Most executable programs intended for command line use provide a formal piece of documentation called a manual or man page. A special paging program called man is used to view them. It is used like this:
```man program```
[Read more on man](http://linuxcommand.org/lc3_man_pages/man1.html)

## Shebang (Unix) #!
In computing, a shebang is the character sequence consisting of the characters number sign and exclamation mark (#!) at the beginning of a script. It is also called sharp-exclamation, sha-bang,[1][2] hashbang,[3][4] pound-bang,[5][6] or hash-pling.[7]

When a text file with a shebang is used as if it is an executable in a Unix-like operating system, the program loader mechanism parses the rest of the file's initial line as an interpreter directive.
> Kindly to try Undertand the code rather than copy the codes


[0-current_working_directory](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/2bf011d8e6954a8327fa0096bc982b73883c9759/0x00-shell_basics/0-current_working_directory) - ```pwd```  prints the absolute path name of the current working directory.

[1-listit](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/1-listit) - ```ls```   Displays the contents list of your current directory.

[2-bring_me_home](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/2-bring_me_home) - ```cd```  Writes a script that changes the working directory to the user’s home directory. You are not allowed to use any shell variables

[3-listfiles](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/3-listfiles) - ```ls - l```  Displays current directory contents in a long format

[4-listmorefiles](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/4-listmorefiles) - ```ls -la```  Displays current directory contents, including hidden files (starting with .). Use the long format.

[5-listfilesdigitonly](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/5-listfilesdigitonly) - ```ls -lna```  Displays current directory contents. Long format with user and group IDs displayed numerically And hidden files (starting with .)

[6-firstdirectory](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/6-firstdirectory) - ```mkdir /tmp/6-firstdirectory```  Creates a script that creates a directory named 6-firstdirectory in the /tmp/ directory.

[7-movethatfile](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/7-movethatfile) - ```mv /tmp/betty /tmp/my_first_directory/```  Moves the file betty from /tmp/ to /tmp/my_first_directory

[8-firstdelete](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/8-firstdelete) - ```rm /tmp/my_first_directory/betty```  Deletes the file betty. The file betty is in /tmp/my_first_directory

[9-firstdirdeletion](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/9-firstdirdeletion) - ```rm -r /tmp/my_first_directory```  Deletes the directory my_first_directory that is in the /tmp directory.

[10-back](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/10-back) - ```cd -```  Write a script that changes the working directory to the previous one.

[11-lists](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/11-lists) - ```ls -la . .. /boot```  Writes a script that lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format.

[12-file_type](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/12-file_type) - ```file /tmp/iamafile```  Writes a script that prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script.

[13-symbolic_link](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/13-symbolic_link) -```"ln -s /bin/ls __ls__```  Creates a symbolic link to /bin/ls, named ls. The symbolic link should be created in the current working directory.

[14-copy_html](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/14-copy_html) - ```cp -u *.html ..```  Creates a script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory. You can consider that all HTML files have the extension .html

[15-lets_move](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/100-lets_move) - ```mv [[:upper:]]* /tmp/u```  Creates a script that moves all files beginning with an uppercase letter to the directory /tmp/u. You can assume that the directory /tmp/u will exist when we will run your script

[16-clean_emacs](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/101-clean_emacs) - ```rm *~```  Creates a script that deletes all files in the current working directory that end with the character ~.

[17-tree](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/102-tree) - ```mkdir -p welcome/to/school```  Creates a script that creates the directories welcome/, welcome/to/ and welcome/to/holberton in the current directory. You are only allowed to use two spaces in your script, not more.

[18-commas](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/103-commas) - ```ls -xamp```  Writes a command that lists all the files and directories of the current directory, separated by commas (,)

[19](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/992434c9399499e96b07620ef6656b6841a68347/0x00-shell_basics/school.mgc) - vi school.mgc
then type in the code below
```
0 string SCHOOL School data
!:mime School
```
exit vi 
then type in the command  
```file -C -m school.mgc```
