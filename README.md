## What is a package manager?

A package manager or package management system is a collection of software tools that automates the process of installing, upgrading, configuring, and removing computer programs for a computer's operating system in a consistent manner.

## Why We Recommend Homebrew

Homebrew installs packages to their own directory on your computer, and then symlinks their files into /usr/local. You can find out more about Homebrew [here](http://http://brew.sh/).

## Installing Homebrew 

 1. type `brew update` to check if Homebrew is installed
 2. type `ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"` to install it
 3. type 'brew update` again - you should get a message about being ready to brew
 
 ## Homebrew related errors
 
 If you installed Homebrew as the root user, Homebrew might be installed, but you might see an error like the below when you try to run a brew command:
 
 `Error: Permission denied - /Library/Caches/Homebrew/Formula/libyaml.brewing` 
  
 Fix that by:
 
 1. Running:
 
- `whoami`
- `ls -lah /Library/Caches`
- `ls -lah /Library/Caches/Homebrew`

 2. If you see "root" in the output of those commands, instead of your username, run the following:
  - `sudo chown -R "$USER":admin /usr/local`
  - `sudo chown -R "$USER":admin /Library/Caches/Homebrew`
 3. Retry the brew commands you were running previously to see if you still have a permissions error.



<p data-visibility='hidden'>View <a href='https://learn.co/lessons/package-manager'>Package Manager</a> on Learn.co and start learning to code for free.</p>
