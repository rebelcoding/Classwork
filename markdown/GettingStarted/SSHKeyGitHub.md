# SSH Key with GitHub

Since we are recommending that you set up an GitHub account, and that you use `ssh` keys, we will go through this process first.

## SSH key pairs
Secure-shell keys are basically really long character sets created by math.

Two keys are created, one for the user to maintain, and the other to be placed in external systems with the `authorized_keys`.

If you are you are just logging into your server, we presume you to be in your `home` directory.

If you want to make sure, you can type the command `cd;` and this command will transport you to your `home` directory.

#### Building the key-pair

Next we will run the command `ssh-keygen -t rsa`.

You can press enter at every promt to accept the default values, and keep the password blank.

If you need to be supersecret agent about it, you can use a password though.

*Only super-secret agents though, as they've take classes to memorize passords and such.*

```bash
newuser@sf-codes:~$ ssh-keygen -t rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/home/newuser/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /home/newuser/.ssh/id_rsa.
Your public key has been saved in /home/newuser/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:4H25vo1c2TFhbvRDEDL6zyEeRJ3C7+5YW newuser@sf-codes
The keys randomart image is:
+---[RSA 2048]----+
|          .+.oo  |
|          oooo.  |
|      .  . .0  = |
|     . o  S. .= o|
|      . S o+..o=.|
|         ..oo*=o+|
|          +.=*.+o|
|         o O=.. .|
|          =+E. . |
+----[SHA256]-----+
newuser@sf-codes:~$
```

#### View the public key id_rsa.pub

After this code has run we want to print out and copy the public key so we can put it in GitHub.

Do this we will use the `cat` command followed by the file we want to print to the terminal.

In this case our file is in the hidden `.ssh` folder, and is a file called `id_rsa.pub`

There is another file called `id_rsa` that we will want to keep secret; if this secret key should ever be compromised, we suggest enacting super-secret agent protocols and rebuilding your ssh key-pair.

```bash
newuser@sf-codes:~$ cat .ssh/id_rsa.pub
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDzJJZ6TVt2gumkwjgk5ZaGY1/V7lHTGN9gaIcBUU/JICibSRZd9sRsG+S38lsIyVM9fr0vEPj2RCiOOcbTRhGpbt8mphtJ+zVqwuABIj+QI9u6PI8HokIXIt5UO6Knp7G/2knIicPiUjN8thoNXq2eVPgUfvmi10mKnQaZt7XzTFJFY80B240OyQJUa6KqQnlIT73+pO6/G4XfkIkI+AbOzQ4D39miy3o25Sna9yqhHc4TsVfZnBbT6Bv1m/ZMmAZkAOFu5Y8k5pqCl8mqa5LujMI9Bt4bbovoZ/g+pMHGX5WJ2YyBWlhM0C9tLB8iNQBce2JrYYTZYdT9w3SmG3uv newuser@sf-codes

```

Highlight the code `ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDzJJZ6TVt2gumkwjgk5ZaGY1/V7lHTGN9gaIcBUU/JICibSRZd9sRsG+S38lsIyVM9fr0vEPj2RCiOOcbTRhGpbt8mphtJ+zVqwuABIj+QI9u6PI8HokIXIt5UO6Knp7G/2knIicPiUjN8thoNXq2eVPgUfvmi10mKnQaZt7XzTFJFY80B240OyQJUa6KqQnlIT73+pO6/G4XfkIkI+AbOzQ4D39miy3o25Sna9yqhHc4TsVfZnBbT6Bv1m/ZMmAZkAOFu5Y8k5pqCl8mqa5LujMI9Bt4bbovoZ/g+pMHGX5WJ2YyBWlhM0C9tL newuser@sf-codes` and it should all be one line - the entire code.

I realize that it looks like 3 separate lines, but that is just because there are spaces between the three strings `ssh-rsa`, `super long set of characters` and `newuser@sf-codes`.

#### Connect to GitHub

Copy this code and open a browser tab to your GitHub account.

Go to Settings > SSH and GPG keys and click the green button to add a new key.

You name name your key whatever you like, we suggest something pertinent, perhaps JupyterKey?

Copy in the we highlighted after using the `cat` command.

You won't be able to use any of the example code as all of the keys have been made incomplete, you will need to use your own results from running the code.

Save your new key and you're all set!