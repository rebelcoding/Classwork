# Basic Git Commands

In this notebook we will cover how to use basic `git` commands.

`git` is a system for version-control. What this means is that it keeps a record of our files, and the changes we make to them. Should we ever need to re-examine a change, `git` has ways of letting us do this.

## `git clone`

First we need to get a repository, and presuming you have an `ssh` registered with a Github account, we can use the command `git clone git@github.com:ScreamFreely/SFCodingClass`

But let's take a close look at what is happening.

`git` this is the program we are running

`clone` is the command we are running within the `git` program

`git@github.com` the `clone` command requires certain parameters, this first one tells the `git` program what domain will be used to used.

`ScreamFreely` once we have the correct domain, we need to identify the correct user, which in this case is `ScreamFreely`.

`SFCodingClass` and lastly, we need to identify the correct repository we want to clone onto our server.

Our structure then is as follows:

`git clone git@github.com:user/repository`

Make sure to include the `:` and `/` symbols correctly.

If your `ssh` key-pair is correctly set up, you ought see the following when you run the code.

```bash
newuser@sf-codes:~$ git clone git@github.com:ScreamFreely/SFCodingClass
Cloning into 'SFCodingClass'...
Warning: Permanently added the RSA host key for IP address '76.60.255.115' to the list of known hosts.
remote: Enumerating objects: 7, done.
remote: Counting objects: 100% (7/7), done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 7 (delta 1), reused 7 (delta 1), pack-reused 0
Receiving objects: 100% (7/7), 10.33 KiB | 3.44 MiB/s, done.
Resolving deltas: 100% (1/1), done.
newuser@sf-codes:~$
```
---
---
## `git pull`

---
---

## `git push`

The `git push` command has a few steps before it will run correctly.

### `git add`

First we will navigate into the correct directory using `cd SFCodingClass`.

Then we will use the command `git add .` to add all of the files from that location *on down the system* that have changed since the code was last ran.

If we wanted to add a specific file we could use the command like this:

`git add folder/specific.file`

But we just want to add all files that have been updated.

```bash
newuser@sf-codes:~/notebooks$ cd SFCodingClass/
newuser@sf-codes:~/notebooks/SFCodingClass$ git add .
newuser@sf-codes:~/notebooks/SFCodingClass$ 
```

### `git commit`



```bash
newuser@sf-codes:~/notebooks/SFCodingClass$ git commit -m 'updated bashcmds and added gitcmds'
[master 219ce42] updated bashcmds and added gitcmds
 4 files changed, 787 insertions(+)
 create mode 100644 .ipynb_checkpoints/BasicBashCommands-checkpoint.ipynb
 create mode 100644 .ipynb_checkpoints/BasicGitCommands-checkpoint.ipynb
 create mode 100644 BasicBashCommands.ipynb
 create mode 100644 BasicGitCommands.ipynb
 newuser@sf-codes:~/notebooks/SFCodingClass$ 
```

### `git push`

```bash
newuser@sf-codes:~/notebooks/SFCodingClass$ git push origin master
Counting objects: 6, done.
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 5.96 KiB | 1.99 MiB/s, done.
Total 6 (delta 1), reused 0 (delta 0)
remote: Resolving deltas: 100% (1/1), done.
To github.com:ScreamFreely/SFCodingClass
   bc1baa6..219ce42  master -> master
newuser@sf-codes:~/notebooks/SFCodingClass$
```

---

## `git status`

```bash
newuser@sf-codes:~/notebooks/SFCodingClass$ git status
On branch master
Your branch is up to date with 'origin/master'.

Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   .ipynb_checkpoints/BasicBashCommands-checkpoint.ipynb
        modified:   .ipynb_checkpoints/BasicGitCommands-checkpoint.ipynb
        modified:   BasicBashCommands.ipynb
        modified:   BasicGitCommands.ipynb

newuser@sf-codes:~/notebooks/SFCodingClass$
```

---
## Git branches
### `git branch`
### `git checkout`