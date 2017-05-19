# Bash Aliases

### Table of Contents
* [Setup](#setup)
* [How they work](#how-they-work)
* [Examples](#examples)

A Bash alias is essentially a keyboard shortcut, an abbreviation, a way to avoiding typing a long command sequence into our terminal. We can make as many of these terminal commands as we like, but I personally only make one when I find myself typing the same command over and over.

### Setup

By default, bash loads the ```.bash_profile``` on startup. Previously, we have added paths and other configurations to this file and we can also put our aliases in this file. However, to keep our files organized we want to create another file to put our aliases in. 

By convention the ```.bashrc``` file is where we want to put these aliases. If it doesn't exist already go ahead and create it.

```bash
$ cd ~
$ touch .bashrc
```

Now we have to tell bash to load this file if it exists. Because ```.bash_profile``` is loaded by default, we will put our code to acomplish this in there.

```bash
# at the top of our .bash_profile
if [ -f ~/.bashrc ]; then
    source ~/.bashrc
fi
```

Now any code we put into our ```.bashrc``` file will be loaded when our ```.bash_profile``` loads. To test that the file is loading add this to the top of your ```.bashrc``` file.

```bash
echo "Loading .bashrc"
```

To get this new code to be loaded we have to reload our ```.bash_profile```. There are two ways to do this. We can quit terminal and start it again. Alternitavly, if we don't want to close our terminal we can just reload our ```.bash_profile``` directly. 

```bash
$ source ~/.bash_profile
```

When you do this you should see ```Loading .bashrc``` printed in your terminal. You can now remove the echo from the top of your ```.bashrc``` file.

### How they work

If, for example, we include ```alias desk="cd ~/Desktop"``` in the ```~/.bashrc``` file, then each ```desk``` typed in the terminal will automatically be replaced by ```cd ~/Desktop```. This alias will take us to our desktop director.

We can put multiple commands in one alias by separating them with a semicolon. Maybe we want to list the contents of our desktop after we arrive. ```alias desk="cd ~/Desktop; ls"``` will first run ```cd ~/Desktop``` then once that completes it will run ```ls```.

You can even make an alias combining two or more aliases. 

```bash
alias dvenv='source ~/Coding_Dojo/Python/venv/djangoVenv/bin/activate'
alias drun='python manage.py runserver'
alias dstart='dvenv; drun'
```

### Examples
These work on my machine but you may have to change file paths to match your machine.

```bash
# navigation
alias desk='cd ~/Desktop; ls'
alias algos='cd ~/Coding_Dojo/Algos; ls'
alias py='cd ~/Coding_Dojo/Python; ls'

# bash
alias rc='vim ~/.bashrc'
alias bp='vim ~/.bash_profile'
alias rb='source ~/.bash_profile'
```


---
[Home](README.md) | [Top](#bash-aliases) | [Intro](Terminal_Intro.md) | [Reference](Terminal_Reference.md) | [Vim](Terminal_Vim.md)
