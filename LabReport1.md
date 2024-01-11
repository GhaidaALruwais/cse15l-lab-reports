# Lab Report 1
*The file system used is lecture one file directory cloned from "https://github.com/ucsd-cse15l-f23/lecture1"*

The root directory is Lecture1. It contains Hello.class, Hello.java, README, and the messages directory.
The messages directory contains en-us.txt, es-mx.txt, fr-ch.txt, and zh-cn.txt files that demonstrate 'hello world' in different languages. 
***
## Using "cd" command
* No arguments and directory as an argument
![Image](cd1.png)
  - In the first command, I used the change directory command ("cd") on the home directory without giving a path for a new directory. Thus, no change happened and the terminal remained in the same directory.
  - In the second command, I used the change directory command ("cd") to move from the home directory to the messages directory. Therefore, the terminal changed the current working directory to the messages directory _[user@sahara ~/lecture1/messages]$_ 
* File as an argument
![Image](cd2.png)
  - I tried to change the directory from the messages directory to the en-us.txt file. An error message appeared "bash: cd: en-us.txt: Not a directory."
  - I concluded that the cd command will not work with a given file argument because it is not a directory. 
  - After the error message, the second command line appeared in the messages directory, so no change occurred.
## Using "ls" command
![Image](Ls123.png)
## Using "cat" command


