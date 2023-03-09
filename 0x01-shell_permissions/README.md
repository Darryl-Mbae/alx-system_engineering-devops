## Common Commands

* id – Display user identity<br>
* chmod - modify file access rights<br>
* su - temporarily become the superuser<br>
* sudo - temporarily become the superuser<br>
* chown - change file ownership<br>
* chgrp - change a file's group ownership<br>




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

* u+x = Add execute permission for the owner.
* u-x  = Remove execute permission from the owner.
* +x = Add execute permission for the owner, group, and world. This is equivalent to a+x.
* o-rw = Remove the read and write permissions from anyone besides the owner and group owner.
* go=rw = Set the group owner and anyone besides the owner to have read and write permission. If either the group owner or the world previously had execute permission, it is removed.
* u+x,go=rx  = Add execute permission for the owner and set the permissions for the group and others to read and execute. Multiple specifications may be separated by commas.


## Changing File Ownership
We can change the owner of a file by using the chown command. Here's an example: Suppose we wanted to change the owner of some_file from "me" to "you". We could:

```[me@linuxbox me]$ sudo chown you some_file```

## Changing Group Ownership
The group ownership of a file or directory may be changed with chgrp. This command is used like this:

```[me@linuxbox me]$ chgrp new_group some_file```

# How to tackle the tasks

[0-iam_betty](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/265fdab20605aa30ac0029ca29bdfaef28a1d17f/0x01-shell_permissions/0-iam_betty) ```su betty```  Script that changes your user ID to betty.

[1-who_am_i](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/6dcef42130dc4a52b263a17fff74dd9c75f94ee6/0x01-shell_permissions/1-who_am_i) ```id -un``` Print the effective user ID of current user. Other alternative is ```whoami```

[2-groups](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/7ad6a162a5c5c4b100346876ff4ed0d4699cd2e6/0x01-shell_permissions/2-groups) ```id -Gn``` Prints all the groups the current user is part of.

[4-empty](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/69543d4d947a4b11c75e0c2209ce5bbacb69de5c/0x01-shell_permissions/4-empty) ```touch hello``` Create an empty file called hello

[5-execute](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/9b8302d4b2e50ce20ae27f8898c38c5e2199eab9/0x01-shell_permissions/5-execute) ```chmod u+x hello```  Add execute permission to the owner of the file or alternatively ```chmod 700 hello```

[6-mutiple permission](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/d088c67183b7bd90d94f9e4d328d7004778f29a3/0x01-shell_permissions/6-multiple_permissions) ```chmod ug+x,o+r hello``` Add execute permission to user and group owner, and read permission to others for file hello

[7-everybody](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/542223a5be42349723e5320bd17675a339531f0e/0x01-shell_permissions/7-everybody) ```chmod +x hello``` Add execution permission to all for file 

[8-James_Bond](https://github.com/Darryl-Mbae/alx-system_engineering-devops/blob/fc50c391dbf6c49617364164b13e3558db723009/0x01-shell_permissions/8-James_Bond)``` chmod 007 hello``` Set permissions for file hello so owner and group don't have any permissions and other users have all permissions. Alternatively ```chmod ug-rwx,o+rwx hello``` would work but not allowed to use , in in the code
