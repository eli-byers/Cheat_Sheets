# Bash Aliases

A Bash alias is essentially a keyboard shortcut, an abbreviation, a way to avoiding typing a long command sequence. By default, bash loads the ```.bash_profile``` on startup. We have added paths and other configurations to this file before and we can put our aliases in this file also. However, to keep our files organized we want to create another file to put our aliases in.

By convention the ```.bashrc``` file is where we want to put these aliases. If it doesn't exist already go ahead and create it.

```bash
$ cd ~
$ touch .bashrc
```

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

<br>
---
<center>[Home](README.md) | [Top](#bash-aliases) | [Intro](Terminal_Intro.md) | [Reference](Terminal_Reference.md) | [Vim](Terminal_Vim.md)</center>
