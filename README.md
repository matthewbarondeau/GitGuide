
# Electrical Engineering Git Guide

## Table of Contents
<!-- TOC -->
- [GIT Background](#git-background)
  - [Introduction to Version Control Languages](#introduction-to-version-control-languages)
  - [Git Background](#git-background)
- [Git Bash](#git-bash)
- [Use with Keil](#use-with-keil)
  - [Importing files to Keil Project](#importing-files-to-keil-project)
  - [Files that need to be shared between computers](#files-that-need-to-be-shared-between-computers)

<!-- /TOC -->

## Git Background

### Introduction to Git
A version control language is a tool that tracks changes to files and provides users a way to review past changes. There are several version control tools available to you for free, but in EE306 and EE319k we will primarily use Git. Git has two large online repositories that grant free accounts, GitLab and GitHub, but we shall primarily use GitHub.

A version control language tracks the status of a directory and can create specific save spots. The user can choose which changes to save and come back to. In programming, we can use version control languages to save points where significant progress in code has been made.

Git was invented by Linus Torvalds. In the years since, it has become a popular tool for programmers and a valuable teaching tool. Git works by keeping track of changes in a repository, with the most recent version called the HEAD. This head is normally what the programmer is currently working on.  

Git works by having a staging area, a working area, and a series of saved commits. First, let me describe the working area. The working area is the files that you are working on. Think of this as the files that appear and that you can change. Git can see all the changes in this working area, but you have to tell git to care about certain files and save their state. This saving process is two fold. First, you need to move the files you care about to a staging area. Then, once you have everything you want to save there, you perform a commit. The commit will move everything in your staging area into the saved commit. In this way, you can create save points in your code as you work.

## Git Utilities
This section shall describe how to use the Git Bash terminal. It shall start with a brief overview of Linux terminal navigation then move on to Git navigation. To start, you need to download Git Bash onto your machine. The link to find Git Bash is here: https://git-scm.com/downloads

### Git Bash

#### Example Commit

### Git Desktop

#### Example Commit

## Use with Keil
This section shall describe how to use git specifically with Keil projects. There will also be a section in which I show the process for adding files between Keil users and pulling them down.

### Example
First, I am going to create a repository on GitHub for my first assignment. Then I am going to push the folder containing my project up to GitHub.

![](Images/Example1.png)

Now, I am going to make several changes and add a few files. The git log below shows my changes but if I wanted a more in depth view I could use git diff with the two commit ID's. An example here would be "git diff 304c667 cf4daa".

![](Images/Example2.png)

From here, I am going to pull this project onto a different computer. With Keil 5, you should be able to see any new files added to the project. If that is not the case, you can manually add them as shown below:

![](Images/Example3.PNG)

![](Images/Example4.PNG)
