# WHAT IS VERSION CONTROL ???

 You might already know a bit about version control, So a Version Control System is just software that lets you manage and keep track of your source code history.         A version control system, or VCS tracks the history of changes as people and teams collaborate on projects together.
 ## Developers can review project history to find out :
Which changes were made?  
Who made the changes?  
When were the changes made?  
Why were changes needed?

### There are many types of version control ,but the three most popular VCS are :
+ GIT 
+ SUBVERSION
+ MERCURIAL

### The two main types of version control system are :
+ __Centralized Version Control System:__   
With centralized version control systems, you have a single “central” copy of your project on a server, but you never have a full copy of your project locally.  
+ __Distributed Version Control System :__  
In distributed version control, each user has their own copy of the entire repository, not just the files but the history as well. 

 We will be talking about __GIT__ which is __distributed version control system__

### ***Wrap-up--***

Remember that the main point of a version control system is to help you maintain a detailed history of the project as well as the ability to work on different versions of it. Having a detailed history of a project is important because it lets you see the progress of the project over time. If needed, you can also jump back to any point in the project to recover data or file.

# Git Terminology
Git is a tool that covered vast terminology  which can often be difficult for new users, or those who know Git basics but want to become Git masters. So, we need a little explanation of the terminology behind the tools. Let's have a look at the commonly used terms.

**Repository / repo**   
A repository is a directory which tracks all changes made to files in your project  over time which is used to communicate with Git. A Git repository is the `. git/ `folder inside a projec, if you delete the `.git/` folder, then you delete your project’s history.

**Commit**   
Commit in git is used to save the state of your project in your local repository, it basically takes a picture of what all your files look like at that moment and stores a reference to that snapshot.Commit is the essential part in git.

**Working Directory**  
The Working Directory is the files that you see in your computer's file system. When you open your project files up on a code editor, you're working with files in the Working Directory.

This is in contrast to the files that have been saved (in commits!) in the repository.

When working with Git, the Working Directory is also different from the command line's concept of the current working directory which is the directory that your shell is "looking at" right now.

**Staging Area / Staging Index / Index**  
To stage a file is simply to prepare it finely for a commit. You can use the index to build up a set of changes that you want to commit together. When you create a commit, what is committed is currently in the index, not what is in your working directory.

**Branch**   
Instead of copying files from directory to directory, Git stores a branch as a reference to a commit. In this sense, a branch represents the tip of a series of commits—it's not a container for commits. The key thing that makes branches incredibly powerful is that you can make save points on one branch, and then switch to a different branch and make save points there, too.The default branch name in Git is master.  

**Checkout**   
In Git, the term checkout is used for the act of switching between different versions of a target entity. The git checkout command is used to switch between branches in a repository.

**SHA**  
A SHA is basically an ID number for each commit. Here's what a commit's SHA might look like: `e2adf8ae3e2e4ed40add75cc44cf9d0a869afeb6` It is a 40-character string composed of characters (0–9 and a–f) and calculated based on the contents of a file or directory structure in Git. "SHA" is shorthand for "Secure Hash Algorithm".

# Installing Git  
To download Git:

+ Go to https://git-scm.com/downloads
+ Download the software for yor operating system!
+ Install Git choosing all of the default options    

Once everything is installed, you should be able to run git on the command line. If it displays the usage information, then you're good to go!


**First Time Git Configuration**  
Beforeyou can start using Git, you need to configure it. Run each of the following lines on the command line to make sure everything is set up.

```
# sets up Git with your name
 git config --global user.name "<Your-Full-Name>"
```

```
# sets up Git with your email
 git config --global user.email "<your-email-address>"
```

```
# makes sure that Git output is colored
 git config --global color.ui auto
```

```
# displays the original state in a conflict
 git config --global merge.conflictstyle diff3
```

```
 git config --list
```
**Git & Code Editor**   
The last step of configuration is to get Git working with your code editor. Below are three of the most popular code editors.

**Atom Editor Setup**   
```
git config --global core.editor "atom --wait"
```
**Sublime Text Setup**   
```
git config --global core.editor"'C:/Program Files/Sublime Text 2/sublime_text.exe' -n -w"
```

**VSCode Setup**   
```
git config --global core.editor "code --wait"
```

# Create A Git Repo From Scratch
Before you can make commits or do anything else with a git repository, the repository needs to actually exist. To create a new repository with Git, we'll use the `git init` command.      
The `init` subcommand is short for "initialize", which is helpful because it's the command that will do all of the initial setup of a repository.

*Required Commands* 
+ `ls` - used to list files and directories
+ `mkdir` - used to create a new directory
+ `cd` - used to change directories
+ `rm` - used to remove files and directories
+ `pwd`- print working directory

**Git Init**       
 Use the git init command to create a new, empty repository in the current directory.
```
$ git init
```  

This will create a hidden `.git` folder inside your current folder — this is the repository where git stores all of its internal tracking data. It holds all of the configuration files and directories and is where all of the commits are stored.     

 Any changes you make to any files within the original folder will now be possible to track. The original folder is now referred to as your working directory.
                                                
*WARNING* : Don't directly edit any files inside the .git directory. This is the heart of the repository. If you change file names and/or file content, git will probably lose track of the files that you're keeping in the repo, and you could lose a lot of work! It's okay to look at those files though, but don't edit or delete them.


**Clone An Existing Repo**         
The `git clone `command is used to create an identical copy of an existing repository.   

The way that cloning relates to Git is that the command we'll be running on the terminal is git clone. You pass a path (usually a URL) of the Git repository you want to clone to the git clone command.

 ___Verify Terminal Location___      
 Now before you clone anything, make sure you are located in the correct directory on the command line. Cloning a project creates a new directory and places the cloned Git repository in it. The problem is that you can't have nested Git repositories. So make sure the terminal's current working directory isn't located in a Git repository. If your current working directory is not in your shell's prompt, type pwd to print the working directory.   

  _Ready? Let's get cloning!_
 ```
  $ git clone <path-to-repository-to-clone>
```
This command:
+ Takes the path to an existing repository  
+ By default will create a directory with the same name as the repository that's being cloned  
+ Can be given a second argument that will be used as the name of the directory    
+ Will create the new repository inside of the current working directory


*Status Update*  
At this point, we have two Git repositories:

the empty one that we created with the` git init` command   
the one we cloned with the `git clone` command  

How can we find any information about these repositories? Git's controlling them, but how can we find out what Git knows about our repos? To figure out what's going on with a repository, we use the git status command. Knowing the status of a Git repository is extremely important.

**Git Status**   
The git status command will display the current status of the repository.
```
$ git status
```
I can't stress enough how important it is to use this command all the time as you're first learning Git.                                           This command will:

+ Tell us about new files that have been created in the Working Directory that Git hasn't started tracking, yet    
+ Files that Git is tracking that have been modified


# Review A Repo's history

**The Git Log Command**   
The git log command is used to display all of the commits of a repository.
```
$ git log
```

By default, this command displays:

+ the SHA   
+ the author   
+ the date    
+ and the message

**Navigating The Log**   
The important keys for Less are:
+ to scroll down, press   
  + `j` or `↓` to move down one line at a time   
  + `d` to move by half the page screen    
  + `f` to move by a whole page screen  

+ to scroll up, press     
  + `k` or `↑` to move _up_ one line at a time    
  + `u` to move by half the page screen
  + `b` to move by a whole page screen    

+ press `q` to quit out of the log (returns to the regular command prompt.

**git log --oneline**    
The `git log` command has a flag that can be used to alter how it displays the repository's information. That flag is `--oneline`:
```
$ git log --oneline
```
This command:

+ lists one commit per line    
+ shows the first 7 characters of the commit's SHA      
+ shows the commit's message

**git log --stat**   
The` git log` command has a flag that can be used to display the files that have been changed in the commit, as well as the number of lines that have been added or deleted. The flag is `--stat` ("stat" is short for "statistics"):
```
$ git log --stat
```
This command:

+ displays the file(s) that have been modified    
+ displays the number of lines that have been added/removed    
+ displays a summary line with the total number of modified files and lines that have been added/removed

**git log -p**   
The `git log` command has a flag that can be used to display the actual changes made to a file. The flag is `--patch `which can be shortened to just -p:
```
$ git log -p
```
This command adds the following to the default output:

+ displays the files that have been modified         
+ displays the location of the lines that have been added/removed     
+ displays the actual changes that have been made

**git show**   
The `git show` command will show only one commit. So don't get alarmed when you can't find any other commits  it only shows one. The output of the git show command is exactly the same as the `git log -p` command.   

This command displays :
+ the commit       
+ the author       
+ the date      
+ the commit message      
+ the patch information

# Add Commits To Repo                 

***Git Add***     
The git add command is used to move files from the Working Directory to the Staging Index.
```
$ git add <file1> <file2> … <fileN>
```
Running the` git add` command produces no output ___as long as there wasn't an error___. So how do we have Git tell us what it did and has happened to the  file that was added? That's what `git status `does. 

This command:   

+ Takes a space-separated list of file names    
+ Alternatively, the period` (.) `can be used in place of a list of files to tell Git to add the current directory (and all nested files)

***Git Commit***          
To make a commit in Git you use the git commit command, but don't run it just yet...go back to the Git configuration step and configure Git to use your chosen editor.   

If you did configure your editor, then go ahead and make a commit using the `git commit` command. Remember, your editor should pop open.
```
$ git commit
```
This command:



+ Takes files from the  _Staging Index_  and saves them in the _repository_.
+ Will open the code editor that is specified in your configuration

Inside the code editor:

+ A commit message must be supplied  
+ Lines that start with a # are comments and will not be recorded   
+ Save the file after adding a commit message   
+ Close the editor to make the commit  

*Bypass The Editor With The -m Flag*   

If the commit message you're writing is short and you don't want to wait for your code editor to open up to type it out, you can pass your message directly on the command line with the -m flag:
```
$ git commit -m "Initial commit" 
```
Be aware that you can't provide a description for the commit, only the message part.

Then, use  `git log`  to review the commit you just made

***Good Commit Messages***         
+ do keep the message short (less than 60-ish characters)    
+ do explain what the commit does (not how or why!)
+ do not explain why the changes are made (more on this below)      
+ do not explain how the changes are made (that's what git log -p is for!)  
+ do not use the word "and"     
+ if you have to use "and", your commit message is probably doing too many changes - break the changes into separate commits.

***Git Diff***   
The git diff command can be used to see changes that have been made but haven't been committed, yet.
```
$ git diff
```
This command displays:

+ the files that have been modified  
+ the location of the lines that have been added/removed   
+ the actual changes that have been made

***Git Ignore***    

If you want to keep a file in your project's directory structure but make sure it isn't accidentally committed to the project, you can use the specially named file, `.gitignore` this file is used to tell Git about the files that Git should not track. This file should be placed in the same directory that the `.git` directory is in.

Globbing lets you use special characters to match patterns/characters. In the .gitignore file, you can use the following:

+ blank lines can be used for spacing  
+ `#`- marks line as a comment   
+ `*`- matches 0 or more characters   
+ `?`- matches 1 character   
+ [`abc`] - matches a, b, _or_ c   
+ `**` - matches nested directories - a/**/z matches   
  + a/z
  + a/b/z
  + a/b/c/z               
          
#  Undoing Changes

 _**Changing The Last Commit**_ 

  If your Working Directory is clean (meaning there aren't any uncommitted changes in the repository), then running `git commit --amend` will let you provide a new commit message. Your code editor will open up and display the original commit message. Just fix a misspelling or completely reword it! Then save it and close the editor to lock in the new commit message.   
  But, amending does not just alter the most recent commit, it replaces it entirely, meaning the amended commit will be a new entity with its own ref.
  ```
  $ git commit --amend
  ```
  then you'd save all of the files that were modified, then you'd use git add to stage all of the modified files (just as if you were going to make a new commit!) ,  but then you'd  run ` git commit --amend ` to update the most-recent commit instead of creating a new  one.

_**Git Revert**_       

The git revert command is used to reverse a previously made commit:
```
$ git revert <SHA-of-commit-to-revert>
```
this will pop open code editor to edit/accept the provided commit message.
This command:

+ will undo the changes that were made by the provided commit  
+ creates a new commit to record the change

_**Git Reset**_         
The  `git reset `command is used erase commits:
```
$ git reset <reference-to-commit>
```
It can be used to:

+ move the HEAD and current branch pointer to the referenced commit  
+ erase commits with the `--hard ` flag
+ move committed changes to the staging index with `--soft` flag        
+ unstage committed changes with `--mixed ` flag

Typically, ancestry references are used to indicate previous commits. The ancestry references are:   

+ `^ ` – indicates the parent commit       
+ `~ ` – indicates the first parent commit

# Tagging ,Branching & Mearging

## Git Tag Command

The command we'll be using to interact with the repository's tags is the git tag command:
```
$ git tag -a <keyid>
```
This will open your code editor and wait for you to supply a message for the tag.
In the command above the` -a`  flag is used. This flag tells Git to create an annotated flag.

Annotated tags are recommended because they include a lot of extra information such as:

+ the person who made the tag        
+ the date the tag was made    
+ a message for the tag     


_Verify Tag_
After saving and quitting the editor, nothing is displayed on the command line so just type `git tag` , it will display all tags that are in the repository.

___Deleting A Tag___

A Git tag can be deleted with the -d flag (for delete!) and the name of the tag:
```
$ git tag -d <keyid>
```
___Adding A Tag To A Past Commit___      

What if you wanted to tag a commit that occurred farther back in the repo's history?   
All you have to do is provide the SHA of the commit you want to tag!
```
$ git tag -a <keyid> <SHA>
```

## Git Branch       
The git branch command is used to interact with Git's branches:
```
$ git branch
```
___Create A Branch___

To create a branch, all you have to do is use git branch and provide it the name of the branch you want it to create, you'd run this command:
```
$ git branch <branch-name>
```
___git checkout___ 

Even though we created the new <branch-name>, no new commits will be added to it since we haven't switched to it, yet. If we made a commit right now, that commit would be added to the master branch. 


To switch between branches, we need to use Git's checkout command.
```
$ git checkout <branch-name>
```
___Branches In The Log___        
The branch information in the command prompt is helpful, but the clearest way to see it is by looking at the output of git log. But just like we had to use the --decorate flag to display Git tags, we need it to display branches.
```
$ git log --oneline --decorate
```
___Delete A Branch___

 If you want to delete the branch, you'd use the `-d `flag. The command below includes the `-d` flag which tells Git to delete the provided branch.
```
$ git branch -d <branch-name>
```
One thing to note is that you can't delete a branch that you're currently on,you'd have to switch.
To force deletion, you need to use a capital `D` flag .
```
git branch -D <branch-name
```

___See All Branches At Once___

Wouldn't it be nice if we could see all branches at once in the git log output
```
$ git log --oneline --graph --all
```
The `--graph` flag adds the bullets and lines to the leftmost part of the output. This shows the actual branching that's happening. The `--all `flag is what displays all of the branches in the repository.



## The Merge Command     
The git merge command is used to combine Git branches:
```
$ git merge <other-branch>
```
There are two types of merges:

+ Fast-forward merge – the branch being merged in must be ahead of the checked out branch. The checked out branch's pointer will just be moved forward to point to the same commit as the other branch.
+ the regular type of merge   
  + two divergent branches are combined                    
  + a merge commit is create

___Merge Conflict___   
When a merge fails, it is called a merge conflict.

A merge conflict happens when the same line or lines have been changed on different branches that are being merged. Git will pause mid-merge telling you that there is a conflict and will tell you in what file or files the conflict occurred. 

___Merge Conflict Indicators Explanation___ 

The editor has the following merge conflict indicators:

+ `<<<<<<<` HEAD everything below this line (until the next   indicator) shows you what's on the current branch  

+ `|||||||` merged common ancestors everything below this line (until the next indicator) shows you what the original lines were   

+ `=======` is the end of the original lines, everything that follows (until the next indicator) is what's on the branch that's being merged in   

+ `>>>>>>>` heading-update is the ending indicator of what's on the branch that's being merged in (in this case, the heading-update branch) 


To resolve the conflict in a file:

+ locate and remove all lines with merge conflict             + indicators   
+ determine what to keep   
+ save the file(s)    
+ stage the file(s)    
+ make a commit   

Be careful that a file might have merge conflicts in multiple parts of the file, so make sure you check the entire file for merge conflict indicators - a quick search for` <<<` should help you locate all of them.