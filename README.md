# My Custom Commands

Just some commands I wrote to make life easier. 

## Installation

Clone this repo to the location of your choice then add the path to $path


### bootstrap.py

This script is my way of create my dotfiles from my dotfiles repo. This coupled with a cloud service allows me to keep
the configuration of multiple systems in sync. Nothing worse then sitting down at home and your shell doesn't have the
all the aliases you are used to using.

### setgit

I found myself juggling a couple of gitconfigs (my personal one linked to my github account and one for my employer's
Github Enterprise Server and wanted an easy solution to switching between configs. So, here we are. This may not be the
most elegant solution but it works for me.

This command basically copies a gitconfig from a source into your .gitconfig allowing you to have multiple gitconfigs.
The only issue is having to juggle them. I actually solve that by just calling the setgit command in my pre-commit hook.

To use just copy your current gitconfig to gitconfig-me.  

Then create your different gitconfigs appending the name with -sourcename. For example .gitconfig-work

To change to your work config you would simply run:
```
setgit sourcename
```
The contents of .gitconfig-sourcename will overwrite the .gitconfig contents.

Then when you want to switchback to your original config run:
```
setgit me
```
