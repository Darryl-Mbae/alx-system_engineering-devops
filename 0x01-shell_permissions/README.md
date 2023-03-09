## Common Commands

* chmod - modify file access rights<br>
* su - temporarily become the superuser<br>
* sudo - temporarily become the superuser<br>
* chown - change file ownership<br>
* chgrp - change a file's group ownership




![](http://linuxcommand.org/images/file_permissions.png)

## chmod
The chmod command is used to change the permissions of a file or directory.

```
rwx rwx rwx = 111 111 111
rw- rw- rw- = 110 110 110
rwx --- --- = 111 000 000

rwx = 111 in binary = 7
rw- = 110 in binary = 6
r-x = 101 in binary = 5
r-- = 100 in binary = 4
-w- = 010 in binary = 2
--x = 001 in binary = 1

```
For example, if we wanted to set some_file to have read and write permission for the owner, but wanted to keep the file private from others, we would:
```
root@/alx-system_engineering-devops/0x01-shell_permissions# chmod 600 some_file

```
## Changing File Ownership
We can change the owner of a file by using the chown command. Here's an example: Suppose we wanted to change the owner of some_file from "me" to "you". We could:

```[me@linuxbox me]$ sudo chown you some_file```

## Changing Group Ownership
The group ownership of a file or directory may be changed with chgrp. This command is used like this:

```[me@linuxbox me]$ chgrp new_group some_file```

# How to tackle the tasks

[0-iam_betty]https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/265fdab20605aa30ac0029ca29bdfaef28a1d17f/0x01-shell_permissions/0-iam_betty
```su betty```  Script that changes your user ID to betty.
