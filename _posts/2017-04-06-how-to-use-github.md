---
layout: post
title:  "Use Github and Git"
date:   2017-04-06 21:52:15 -0700
tags: [Github]
categories: [howto]
---


How To Use GitHub (and Git)
===========================
*Note: This document by [Lee](http://github.com/lee2sman), updated April 2017*

# Find, Share and Collaborate On Code

GitHub is a website for hosting code. Created in only 2008, in the past few years it has exploded as the central site where people go to find, share and collaborate on writing code, in any programming language. As of the time of this writing, there are close to 10 million users and 21 million repositories of code. It is the largest host of code in the world.

When we talk about code and scripts, we are really talking about text. GitHub can also be used to host any text: documentation, wikis, data, even vector image files. 

# Searching for code

You can use [GitHub](http://github.com) as a site to search for code. Thousands (millions) of software code can be found on GitHub that you can learn from, or even often use in your own programs. Type in a topic or program that you are looking for and search. On the left side of the results you'll notice that it breaks down code by Language. Click on one of the languages and it will show you only the code written in that languages. You might notice Shell as one option to see shell scripts. 

If you click on a project name it opens up a repository with all of its files. A repository, also known as a *repo*, is the directory containing all of the files relating to a single piece of software. This will usually include a README file where the programmer includes information. Sometimes they put info on how to run the software, how to install it, list dependencies such as libraries you might need to install first to use it, or any other notes. Above the README text you should see other files that can include code and folders and potentially other files such as images.

# Using code you find on GitHub

The simplest way to use GitHub is as a tool for finding code. If you find code you want to use, you click on its name to open it up in an online text display, then click on the RAW button in the top right to get just the program code. You can copy this and paste it into a text editor, or save it directly to your computer. You should look for a license in the repo listing the permissions for the code. Though many of the repos don't have a license posted.

That said, it's proper form to fork code on GitHub. If you click the Fork button it will create an exacty copy of the repository in your own GitHub account. It will ask you for a name (you can keep the same name) and when you click okay it will bring you into your new repo folder, where underneath the name it will say where the original repository was forked from. The original programmer will be able to see that you forked their code as well as any edits you make. Later you can attempt to merge your changes with the original repository if you have significant improvements.

# What Is Git?

In addition to the website GitHub, it's important to understand the underlying structure behind the storing and sharing of code, as well as how it relates to software on your computer. 

GitHub works with software and connects to your computer, traditionally through the command line. In addition to GitHub, there is a separate piece of software called Git. Git is a source code version control system. It is a series of "commits" or snapshots of your code. You make these commits manually. Imagine you make a change to text in Microsoft Word, and then you hit undo, and then undo again, and then again. Each of those different variations on your text could be saved as a different *commit,* allowing you to go back and forth in your code to earlier or later versions. You might even split your code into a version for Mac and another version for Windows and another for Linux. This is what we mean by *Version Control.*

# Why Use Git and GitHub

Git is the commandline software you use to track changes to your code.

GitHub is the place where you can store and share that code online, find and fork others' code, and collaborate on software with others.

Git and GitHub connect together through the command line on your computer.

# 2 models of Version Control

There are 2 different models for how version control can work. In a *centralized* model, each person can *check out* code, modify and save that code, and then check that code back in so that other people can work with it. In essense, only one person at a time can alter the code. This ensures that all collaborators are up to date with the latest model.

In a *distributed* system, each person keeps their own local repository for the software they are writing together. When you make changes you want to share, you have to *check in* your code with the main online copy and reconcile any differences so that the two merge together into a single match. GitHub is this style of version control.

# A theory of Git and GitHub Together

Git is fast. It's distributed easily across computers. Every *commit* is tracked so that you can return to it if necessary if you make a mistake later. Every writer of a piece of software has a local version of the program that they work on. You add and commit your code on your own computer with Git, and when you are ready you push it online to your repository on your github page.

If you fork (aka copy) someone else's code or program, you pull it onto your computer so that you can edit the code. Afterward, you can push it to your own online repository or you can submit a *pull request* to the original code and that person will look at your code and decide to merge the two together (or not).

# Signup for GitHub

[Signup](https://github.com/) for an account on Github

# Thinks to do on GitHub.com

* Follow coder-people you like to see their repos
* Search by language
* Fork others' projects

# How To Use Github via The Web

#### Useful info on Github's Help pages

[Add a file](https://help.github.com/articles/adding-a-file-to-a-repository/) to your own repository.  
[Add a file to someone else's repository](https://help.github.com/articles/editing-files-in-another-user-s-repository/)  


# Setting up Git On The Commandline

1. Install [Git](http://git-scm.com/downloads).
2. Open the Terminal (Mac) or the Git Bash app you installed (Windows) or other command line (Linux). 
3. Set your default name. Run ```git config --global user.name "Your Name Here"```
4. Set your default email. Run ```git config --global user.email "your_email@youremail.com"```

# Basic Git Commands

```git init``` Initializes a new Git repository so that it is being tracked by git. Once you run this you can now run ```git``` commands in the directory.

```git config``` Config stands for “configure” and is useful when you set up Git for the first time.

```git help``` This command tells you the 21 most common git commands or type ```git help <command>``` for info on a specific command.

```git status``` Check the status of your repository. What files still need to be committed? What branch are you working in?

```git add <filename>``` This command tells git to pay attention to the specified file, before you commit it.

```git commit``` This is the most important command. After making changes to a file  where you feel you want to save that particular version you commit those changes. The standard way to use this is ```git commit -m “Message here.”``` The -m specifies you are adding info on this commitment, and it's normal to put a short explanation of your most recent changes such as ```git commit -m "updated readme file"```

```git push``` After working on your local computer for a while and you want your commits to be visible online on GitHub you “push” the changes up to GitHub with this command. As an example ```git push origin master```.

```git pull``` When working on your local computer and want the most up-to-date version of your repository to work with this pulls the changes down from GitHub.

```git remote add origin <repoLocation>``` Used to connect your local repo with the remote (online) one.

# Git Commands When Working With Collaborators

```git branch <newBranchName>``` If you are working with multiple collaborators but want to make changes on your own this command is to start a new branch. Essentially this is a new timeline of commits, of changes and file additions that are just from you. Your title goes after the command.

```git checkout <repoName>``` This allows you to “check out” a repository that you are not currently inside if you were working in a different branch. For example if you are working on myVersion you do ```git checkout master``` to look at the master branch.

```git merge``` After finishing work on a branch you can merge your changes with the master branch. ```git merge myVersion``` would take the changes you made to your branch and add them to the master.


# Standard Way To Create A Repo

1. Go to [Github.com](http://github.com) and click plus and New Repository.
2. Give it a name and short description. Let's call this MyProject. Click the *Create Repository* button.
3. Go back to the terminal. Type ```mkdir ~/MyProject``` to make a directory (folder) called MyProject inside your home folder.
4. To get into that folder, we type ```cd ~/MyProject```. ```cd``` means change directory. It lets us navigate through folders on our computer in the command line.
5. We're inside the folder. We type ```git init``` to initialize it and have git track its changes.
6. Let's make a readme file. Make a file called README ```touch README.md```. Open it in ```nano```, type a description or whatever you want in your README and save it with a .md extension. 
7. Type ```git status``` to see if git notices there's a new file. It should say that there is an *untracked* file.
8. ```git add ReadMe.md``` to track the file
9. ```git commit -m "Initial commit of ReadMe"``` The m indicates we're saving a message about what we're doing.
10. We want to push these changes online. First we need to connect our local folder on our computer to the online repo. ```git remote add origin https://github.com/username/myproject.git``` The url we get from our repo's page on github.com.
11. Now let's push our local changes to our online repo we just connected. ```git push origin master```
12. Refresh your github page online and you should see those changes.

 
# More Git

Lots more tutorials and good info on Github [Help](https://help.github.com/) page.
