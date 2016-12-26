# Intro to Terminal
This is a quick tutorial to show you how to use some of the basic comands. Follow along in your terminal. To start, open a new terminal window. This is Bob Bobs terminal but you should see something like this.

```bash
Bobs-MacBook:~ bbobs$
```

This is called the command prompt. It shows the name of the computer you are in, the current directory (folder), the username of the current user, then a dollar sign. In the above example, the computers name is ```Bobs-MacBook```, the current directory is ```~``` meaning your home folder, and the user is ```bbobs```.

As we move forward, enter the code after the ```$``` to follow along. The lines stating with ```#``` are comments not commands or output.

#### List the contents of the current directory
```bash
Bobs-MacBook:~ bbobs$ ls
# The output should look something like this
Applications Downloads    Music        Public       Desktop      
Library      Pictures     Sites        Documents    Movies
```
#### Navigate into the Documents folder
```bash
Bobs-MacBook:~ bbobs$ cd Documents
# Your command prompt should change showing your current directory to be Documents
Bobs-MacBook:Documents bbobs$
```
#### List the contents of Documents
```bash
# The output will contain a table of every file and directory in Documents
# Lets say there is a folder called Notes a file called todo.txt
Bobs-MacBook:Documents bbobs$ ls
Notes    todo.txt
```
#### Make a new directory called CodingDojo and one inside that called Terminal
```bash
Bobs-MacBook:Documents bbobs$ mkdir CodingDojo
Bobs-MacBook:Documents bbobs$ mkdir CodingDojo/Terminal
Bobs-MacBook:Documents bbobs$ ls
CodingDojo Notes      todo.txt  
```
#### Create a file called notes.txt in the new Terminal directory
```bash
Bobs-MacBook:Documents bbobs$ touch CodingDojo/Terminal/notes.txt
Bobs-MacBook:Documents bbobs$ cd CodingDojo
Bobs-MacBook:CodingDojo bbobs$ ls
Terminal
Bobs-MacBook:CodingDojo bbobs$ cd Terminal
Bobs-MacBook:Terminal bbobs$ ls
notes.txt
```
#### Whats the path to our working directory?
```bash
# In the output 'yourusername' will be your username
Bobs-MacBook:Terminal bbobs$ pwd
/Users/yourusername/Documents/CodingDojo/Terminal
```

#### Remove the directories and file we created
```bash
Bobs-MacBook:Terminal bbobs$ cd ../../
Bobs-MacBook:Documents bbobs$ ls
CodingDojo Notes      todo.txt  
Bobs-MacBook:Documents bbobs$ rm -r CodingDojo
Bobs-MacBook:Documents bbobs$ ls
Notes    todo.txt  
```

<br>
---
<center>[Home](README.md) | [Top](#intro-to-terminal) | [Terminal Reference](Terminal_Reference.md)</center>
