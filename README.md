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

# sets up Git with your email
 git config --global user.email "<your-email-address>"

# makes sure that Git output is colored
 git config --global color.ui auto

# displays the original state in a conflict
 git config --global merge.conflictstyle diff3

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