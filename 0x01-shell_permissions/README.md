chmod - modify file access rights<br>
su - temporarily become the superuser<br>
sudo - temporarily become the superuser<br>
chown - change file ownership<br>
chgrp - change a file's group ownership




![](http://linuxcommand.org/images/file_permissions.png)

chmod
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



