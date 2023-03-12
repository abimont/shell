# Shell: Permissions

On a Linux system, each file and directory is assigned access rights for the owner of the file, the members of a group of related users, and everybody else. Rights can be assigned to read a file, to write a file, and to execute a file, and are modified by the following commands:

- `chmod`: modify file access rights.
- `su`: temporarily become the superuser.
- `sudo`: temporarily become the superuser.
- `chown`: change file ownership.
- `chgrp`: change a file's group ownership.

### How to see the permission settings for a file?

To see the permission settings for a file, you can use the ls command. As an example, you will look at the bash program which is located in the /bin directory:

```
$ ls -l /bin/bash
-rwxr-xr-x 1 root root 1113504 Jun  6  2019 /bin/bash
```

Here you can see:

- The file "/bin/bash" is owned by user "root".
- The superuser has the right to read, write, and execute this file.
- The file is owned by the group "root".
- Members of the group "root" can also read and execute this file.
- Everybody else can read and execute this file.

In the diagram below, you see how the first portion of the listing is interpreted. It consists of a character indicating the file type, followed by three sets of three characters that convey the reading, writing and execution permission for the owner, group, and everybody else.

![Permissions diagram](http://linuxcommand.org/images/file_permissions.png)

Each file in this directory contains the answer corresponding to the exercises proposed in the "Shell, Permissions" project, developed as part of the Holberton School training.
