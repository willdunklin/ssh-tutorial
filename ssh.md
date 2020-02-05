# How to Create and Read Files on a Remote Server

**OUTLINE:**
1. Connecting to a server via ssh
2. Navigating the user directory
3. Creating directories and files
4. Writing and reading to files


NOTE: the ``$`` indicates the use of the command line. Do not copy the ``$`` while typing commands.

----------------------------------
#### 1.
First things first we need to connect to the remote server. To get started, in a command line (terminal for linux/mac, cmd/powershell for windows).
```
$ ssh username@ip.address
```
Enter password to connect.

----------------------------------
#### 2.
Now we're connected to the server, it is useful to get acquainted with traversing directories.
Here are some basic commands to get started.
Print working dircetory:
```
$ pwd
```
List all files in current directory verbosely:
```
$ ls -al
```
Change directory to ``~`` (home directory):
```
$ cd ~
```
Now we're at the home directory and ready to get started file creation.

----------------------------------
#### 3.
A necessary function is to make new folders to create file structures and organization.
To make and relocate to a new directory:
```
$ mkdir test
```
```
$ cd test
```
Now we make a new file:
```
$ touch hello.txt
```
```
$ ls -al
```
With that list all command we can see that there is a new file in our test directory.

----------------------------------
#### 4.
To access and edit that file with a text editor we can use ``nano``:
```
$ nano hello.txt
```
Try to write something in ``nano``, it doesn't matter what for now.
Once you're done, do ``^O ^X`` to save and exit.
```
$ ls -al
```
To read back the contents of what you just wrote in ``hello.txt`` we can use ``cat``:
```
$ cat hello.txt
```
Now say we aren't happy with the contents of ``hello.txt``. We can append a new line to the file using the ``>>`` operator.
```
$ echo "Hello" >> hello.txt
```
```
$ cat hello.txt
```

----------------------------------
Now we have sucessfully created our very own directory and file. This skillset is integral to interacting with remote linux servers and creating file structures through command line.
