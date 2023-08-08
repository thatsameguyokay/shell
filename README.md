## 2.2.2. Basics of shell script[]: # Path: readme.commands.md

#### chmod: change mode / user permissions

When we create a shell script file, we don't have permissions to execute it on a linux machine. We need to grant the executable permission to the file.

`chmod` command can alter permissions in 3 domains, admin, group and current user. `ch` stands for `change`, `mod` stands for `mode`.

We can grant people with permissions using numbers, and numbers can do wonders:

- 1: used to execute permission
- 2: used to write permission
- 4: used to read permission

In order to grant permissions, we specify the number on index of the user, group or admin. For example, if we want to grant the user with read and write permissions, we can use the following command:

> chmod 6 file.sh

But if we want to grant the user with read, write and execute permissions, we can use the following command:

> chmod 7 file.sh

If we want to grant the user and his group with read only permission, we can use the following command:

> chmod 44 file.sh

The thing is, the number 7 is the sum of 4, 2 and 1. Only 4 is used to give only read permissions to the current user. But if we want to grant the user and his group with read and write permissions, we can use the following command:

> chmod 66 file.sh

Try create a pattern in your mind so you remember this, cmon you're not that dumb.

Default commands data cannot be piped to a file, because it is not a command, it is a shell feature. But we can use the following command to redirect the output to a file:

> set > file.txt

To find a file:

> find / -name file.txt

where / is the directory to find the file in

Following are some important commands:

#### shebang

Shebang is a special character sequence that tells the shell which interpreter to use for the rest of the file. It is used in the first line of the file.

> #!/bin/bash || #!/bin/sh || #!/usr/bin/ksh || #!/usr/bin/sh

#### history

`history` command is used to display the history of commands that we have executed in the terminal.

#### man

`man` command is used to open a guide for any command, similar to `help` command in windows.

#### pwd

`pwd` command is used to display the current working directory.

#### ls -ltr

`ls -ltr` command is used to display the list of files in the current working directory in a long format, sorted by time in reverse order.

#### nproc

`nproc` command is used to display the number of CPUs in the machine.

#### lscpu

`lscpu` command is used to display the details of the CPUs in the machine.

#### free

`free` command is used to display the amount of free memory in the machine.

#### top

`top` command is used to display the list of processes running in the machine, similar to task manager in windows.

#### df

`df` command is used to display the amount of free disk space in the machine.

#### free

`free` command is used to display the amount of free memory in the machine.

#### grep -i

`grep -i` command is used to search for a string in a file, ignoring the case, when accompanied with ps command, it can be used to search for a process.

#### ps -ef

`ps -ef` command is used to display the list of processes running in the machine.

#### kill -9

`kill -9` command is used to kill a process.

#### killall

`killall` command is used to kill all the processes with a given name.

#### | (pipe)

`|` command is used to pipe the output of one command to another command.

For eg: `ps -ef | grep -i java` will display the list of processes with the name java.

#### > (redirect)

`>` command is used to redirect the output of a command to a file.

#### >> (append)

`>>` command is used to append the output of a command to a file.

#### trap

`trap` command is used to trap a signal and execute a command when the signal is received.

Syntax: `trap "command" signal`
