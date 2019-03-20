# Basic Bash Commands

In this notebook we cover basic bash commands with introductory details.

---
### `whoami` & `pwd`

Our first to commands are basic *who am I* and *where am I*.

Definitely things you want to know when you're messing around on the command line.

`whoami` get the name of the user and see that name returned in the terminal.

```bash
newuser@sf-codes:~$ whoami
newuser
```

`pwd` tells us our *present working directory*, or where in the system we are currently located.

Usually after signing into a system you will be directed to the user's home directory, that is the case in our hypothetical system

The terminal returns `/home/newuser` when `pwd` is entered.

```bash
newuser@sf-codes:~$ pwd
/home/newuser
```
---
---
### `ls`
Our next question is *what* is around us in our `pwd`?

For this we use the `ls` command to list the items in a directory

On our system there is only one item in our home directy, and `notebooks` is returned when we input the command `1s`

```bash
newuser@sf-codes:~$ ls 
canin@sf-codes:~$ ls
notebooks
```

---
### `cd`

*How* do we get into that directory?


We use the command `cd` change directory.

Notice what changes?

Systems can be setup differently though often enough it will have some variation of the following format:

`user` @ `system-hostname`: `pwd` $

After the `$` commands are seen when input.

When we changed directories our `pwd` directory changed from `~` to `~/notebooks`

```bash
newuser@sf-codes:~$ cd notebooks
newuser@sf-codes:~/notebooks$ 
```

---
### Command flags

We already know the `ls` command to list the items in a directory, but we only got the names of the items and no details!!

Let's augment our `ls` command with the use of a *flag*, and in this case we will use the `l` flag.

Our commnd will look like this: `ls -l`.

Notice how a `-` is used to signify our flag.

Using this flag we are shown the details of the files in our designated directory.

```bash
newuser@sf-codes:~/notebooks$ ls -l
total 148
drwxr-xr-x 4 newuser newuser  4096 Mar 15 19:59  screamfreely.github.io
-rw-r--r-- 1 newuser newuser  6432 Mar 18 18:31 'DailyAgenda.ipynb'
-rw-r--r-- 1 newuser newuser   887 Mar 14 16:03 'HTMLExam.ipynb'
drwxr-xr-x 2 newuser newuser  4096 Mar 18 19:39  MyScrapers
drwxr-xr-x 4 newuser newuser  4096 Mar 20 00:45  SFCodingClass
-rw-r--r-- 1 newuser newuser 99694 Mar 14 16:03  StLouisPark-Canin.ipynb
-rw-r--r-- 1 newuser newuser    82 Mar 14 16:04  test.py
```
We won't go over what everything means yet (I'm just starting this file), though observe the difference between `screamfreely.github.io` with `drwxr-xr-x` and `DailyAgenda.ipynb with `-rw-r--r--`.

Can you tell which one is a directory and which one is a file?
 
--- 

### `cp` & `mv`

We have finished a few scrapers, and we need to copy, or move, them into our MyScrapers folder.

We'll copy them first using the `cp` command.

Using the command first we list the file we want to copy, `StLouisPark-Canin.ipynb`, followed by where we want to put the file, which in this case is `MyScrapers`.
 
 ```bash
newuser@sf-codes:~/notebooks$ cp StLouisPark-Canin.ipynb MyScrapers
newuser@sf-codes:~/notebooks$
```
If we wanted to move a file we use the `mv` command and the same structure.
 
 ```bash
newuser@sf-codes:~/notebooks$ mv StLouisPark-Canin.ipynb MyScrapers
newuser@sf-codes:~/notebooks$
```

Perhaps you would like to copy an entire directory?

For this we will augment our `cp` command with the `r` flag.

It is worth noting that `r` stands for recursive, which means that whatever is being copied, everything within that will be copied as well, as well as everything within that next level, and so on.

If we do not use the `r` flag, only an empty directory with the same name will be copied.

 ```bash
newuser@sf-codes:~/notebooks$ cp -r MyScrapers SFCodingClass
newuser@sf-codes:~/notebooks$
```

___
___

### `man`

If you ever need more information about a command you can read the command's *manual* using the `man` command.

You will presented with a bunch of information and may be lost as to how to navigate what you see before you!

`j` down

`k` up

`l` right

`h` left

`q` quit

Now you know!

 ```bash
newuser@sf-codes:~/notebooks$ mv StLouisPark-Canin.ipynb MyScrapers
PWD(1)                                                 User Commands                                                 PWD(1)

NAME
       pwd - print name of current/working directory

SYNOPSIS
       pwd [OPTION]...

DESCRIPTION
       Print the full filename of the current working directory.

       -L, --logical
              use PWD from environment, even if it contains symlinks

       -P, --physical
              avoid all symlinks

       --help display this help and exit

       --version
              output version information and exit

       If no option is specified, -P is assumed.

       NOTE: your shell may have its own version of pwd, which usually supersedes the version described here.  Please refer
       to your shells documentation for details about the options it supports.

AUTHOR
       Written by Jim Meyering.

REPORTING BUGS
       GNU coreutils online help: <http://www.gnu.org/software/coreutils/>
       Report pwd translation bugs to <http://translationproject.org/team/>

COPYRIGHT
       Copyright  ©  2017  Free   Software   Foundation,   Inc.    License   GPLv3+:   GNU   GPL   version   3   or   later
       <http://gnu.org/licenses/gpl.html>.
       This is free software: you are free to change and redistribute it.  There is NO WARRANTY, to the extent permitted by
       law.
```
 