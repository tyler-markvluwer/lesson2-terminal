# lesson2-terminal
Your ability to use the terminal well can mean the difference between a 10 hours project and a 5 hour project.

## Purpose:
For both speed and accuracy it is important to know how to use the terminal and shell scripts effectively. We will cover both here.

## Shell scripts:
### Usage:
Lets start by running a simple shell script. If you have cloned this repo you will see a file called 'test.sh'. Navigate to the directory containing this file and simply run 'sh test.sh'. This will execute the contents of the script. What is the script? Well you should open it up and see, but in its simplest form it is the exact same commands that I would normally type into the terminal. The advantage is that I can now run all these commands with only a single terminal command. If you find yourself running the same series of commands over and over again, MAKE A SCRIPT!
### Shortcuts:
You can also create shortcuts using bash style stuff. For instance, if I am super sick of typing 'git commit -m {message}', I can create an ALIAS so that I can now type 'gcm {message}'. Much better than before! But how? In your bash profile (likely located at ~/.bash_profile) add the following lines: 

shopt -s expand_aliases # allow expansion on commands. Only needs to appear in file once.
alias gcm='git commit -m $1'
alias gs='git status'

There are also other use cases, like going to a deeply nested directory which you need to access often. Try out something like the following:
alias gtd='cd /Users/tmarkvluwer/Documents/code/dynamite' # Simple command for going to dynamite directory
## Terminal Navigation:
As seen in lesson1, you can use things like command+arrow, or option+arrow, ctrl+a, ctrl+e, command+shift+{
Another good thing to use is terminal tabs. Using command+t will make a new tab. It is good to have dedicated tabs for dedicated tasks.

## Advanced Terminal Commands:
There are also more advanced commands.

### Joining two commands:
If you want to change directories, and then make a directory do something like the following:
cd myDirec && mkdir newDirec

### Background processes:
If you want launch something as a background process, end it with a single ampersand. This will come into use when you start using brocolli, but a simple use case is as follows:
(sleep 5 && mkdir outerDir && mkdir outerDir/innerDir) &

This will wait 5 seconds, make a directory, and then make another directory inside of the 1st directory. The nice thing is that you don't have to wait for the whole thing to finish before you can use your terminal window again. It runs in the background and you can use your open window for other things. The only downside is that if you start an infinitely running command, you will have to manually kill it. ctrl+c will not work...

### Clearing your window:
If you are on mac or linux you can use ctrl+l, and it will make it "look" like it has been cleared, but you can still scroll up, to see your history. If you are on Mac, you can truly clear it by using command+k. This can come back to bite you though, if you needed some output from above.

### Reverse Search:
Possibly the most useful command of all. ctrl+r is a reverse history search. Simply search part of the command that you ran in the past, and scroll through them in reverse order by repeatedly pressing ctrl+r. When you find the command you are looking for, simply press the right arrow, and the command is 'pasted' into your terminal, where you can now modify or run it.

### ctrl+u / ctrl+y
ctrl+u will cut everything to the left of your cursor and paste it into a secondary clipboard. You can then repaste it using ctrl+y. This is especially useful if you are in the process of writing out a long command, and then remember you were supposed to write another command first. Simply press ctrl+u, and save your typing instead of throwing it away! re-paste it using ctrl+y when you are ready to resume typing the original command.

### More:
There are plenty of lists like this on the internet. Give them a look and find useful things. There's no reason for me to re-type what already exists on a million blogs.
