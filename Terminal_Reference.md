# Terminal Reference
To learn more about any specific command use the ```man``` command in your termianl. For example, ```$ man cd ``` will show you the manuel of the ```cd``` command. Type ```q``` to quit the manuel.

If you are new to Terminal check out the [Terminal Intro](Terminal_Intro.md).


###Table of Contents
* [Files & Directories](#files--directories)
	* [List Contents](#list-contents-ls)
	* [Print Working Directory](#print-working-directory-pwd)
	* [Change Directory](#change-directory-cd)
	* [Make Directory](#make-directory-mkdir)
	* [Make File](#make-file-touch)
* [Editing](#editing)
	* [Move & Rename](#move--rename-mv)
	* [Delete](#delete-rm)

<br>
## Files & Directories

### Directories
A directory is just a fancy name for a folder. Everything in our computer is organized into directories. There are directories within directoies within directories.

The highest level directory is called root, or ```/```. This is what you are seeing when you open your hard drive in finder. Everything in your computer can be accessed from root, stepping down into directories until you are at the same level as a specific file or directory. This address is called a path.

### Files
The most common thing in a computer is a file. There are sound files, image files, text and many other kinds. Most files are visible but files that start with a ```.```, 	```.bash_profile``` for example, are hidden by default. Every file had a path from root, this is besically an address.

A ```note.txt``` file on your Desktop has a path something like this: ```/Users/yourusername/Desktop/note.txt```. It starts at root, ```/```, and shows the higherarchy of folders the file is in, finally ending with ```/filename.extension```. With this path you can point directly to that file from anywhere in the computer.


-
### List Contents: ```ls```
* When we are is a directory we often want to see the contents of that directory. Here are a few of the most common ways to list the items in the current directory.

	```bash
	$ ls		# shows a table of visible items
	
	# There are options you can add to make ls work dirfferently
	$ ls -l		# shows a list of visible items and info about them
	$ ls -a		# shows a table of all items including hidden ones
	$ ls -la	# shows a list of all items and info about them
	```

### Print Working Directory: ```pwd```
* This command displays the path from root to the current directory you are in. It can be usful if you forget where you are, or to create an alias to the current directory, we will talk about this later.

	```bash
	# navigate to the Desktop
	$ cd ~/Desktop
	$ pwd
	/Users/yourusername/Desktop		# 'yourusername' will be your username
	```

### Change Directory: ```cd```
* The cd command is probably the most common command. This is how we navigate around our computer in terminal.

	```bash
	$ cd myDir 		# Moves you into a folder called myFolder in your current derectory
	$ cd ..			# Moves you up one level, out of the directory you are currently in
	$ cd ../myDir	# Moves you into a folder called my myDir that is up one level
	```

* There are a few special directories that have shortcuts to them

	```bash
	$ cd / 		# Moves you to the root directory of your computer
	$ cd ~ 		# Moves you to your home folder
	```
* All absolute file paths start from ```/```.
* You can shorten file or directory paths by starting at ```/``` or ```~```.
* Ex. ```cd ~/Desktop``` takes you to your Desktop directory.

	
### Make Directory: ```mkdir```
* We often need to create new directories. ```mkdir``` and then a name creates a new directory in your current directory. You can give the directory a path to create it somehwere else. 

	```bash
	$ mkdir myNewDir 		# create a folder called myNewDir in the current direcory
	$ mkdir ../myNewDir		# create a folder called myNewDir up one level
	$ mkdir ~/notes			# create a folder called notes in your home folder
	```

### Make File: ```touch```
* Touch was origionally used to updated the last edited timestamp of a file, but if the file doesn't exist, it creates it instead. Now it is most commonly used to create blank files.

	```bash
	$ touch index.html				# create index.html in the current directory
	$ touch templates/index.html 	# create index.html in the local templates directory
	$ touch ~/Desktop/note.txt		# creats note.txt on your desktop
	```

<br>
## Editing
We often have the need to move, rename, or delete some file or derectory. The commands that do this work the same for files and directories alike.

-

### Move & Rename: ```mv```
* The move command will move a file from one location to another, and remove the original. If you move a file to the same directory as it is currently in it will simplally rename it.

	```bash
	# move
	$ mv someFile.ext someDir/someFile.ext	# Moves file someFile.ext into the directory someDir
	$ mv someFile.ext ../someFile.ext		# Moves file someFile.ext up one level
	$ mv myDir otherDir/myDir				# Moves the directory myDir into another directory otherDir
	
	# rename
	$ mv someFile.ext newName.ext			# Renames the file someFile.ext to newName.ext
	$ mv myDir newDirName 					# Renames the directory myDir to newDirName
	```


### Delete: ```rm``` 
* The remove command is very powerful, it removes what ever you tell it to and there is no going back. The files or derectories don't get moved to the trash, if you remove something it is gone. Be very sure you know what you are doing when using this command.

	```bash
	$ rm myFile.ext			# Removes the file myFile.ext
	
	# remove directory and all the files and directories it contains
	$ rm -r myDirectory		# the -r option stands for recursive, it will delete everything
	```


<br>
---
<center>[Home](README.md) | [Top](#terminal-reference) | [Intro](Terminal_Intro.md) | [Vim](Terminal_Vim.md) | [Bash Aliases](Terminal_Bash_Aliases.md)</center>

