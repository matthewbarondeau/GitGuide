#### Git commands
This section shall cover some basic git functionality. I will explain how to use git specifically with Git Bash and normal git command line utilities.

###### git clone
The first idea covered here is cloning. That is, making a local copy of a repository that is stored up on GitHub or GitLab. This is normally the first step in the process of using git.

To start, you need to have a repository on GitHub or GitLab, and grab the HTTPs link. You need this link so that you can safely copy the code onto your machine. An example of finding the HTTPS link and cloning the repository is shown below.

![](Images/clone.png)

###### git status
So, now what? We have cloned a repository from GitHub, but we don't know what git is tracking or what is going on. A way to view what changes have been made or that git is tracking, is through the "git status" command. This command spits a lot of information at you. So I'm going to put a screen capture right below here, and then explain what is going on.

![](Images/status.png)

Alright so lets look at all these sections. First, up at the top, it tells us that we are up to date with the remote branch up on GitHub. If there were additional commits on our computer that weren't pushed up, or additional changes that we haven't pulled down, this will tell us.

Right below that is a section with some green letters in it. This is the contents of the staging area. As I mentioned above, these are the files that we want to add to a commit. In the commit process described below, these are the changes that will be saved.

Below the green area is the red area. These are the changes that happened in the directory, but that git is not currently tracking. We can move them to the staging area using the add comand below.

###### git add
Once you have cloned the repository, you can create your files or move them into this repository. At this point however, git is not tracking them. To tell git to begin tracking files, I will use the "git add filename" command. This command will add any file I name to the staging area that I mentioned earlier. If I want to add every file in the repository, I can use "git add ."

An example of git add is shown below:

![](Images/add.png)

###### git commit
Alright, now we have finally reached the commit. Once we have added an item into the staging area using git add, we need to permanently save our changes. This is the commit process. The syntax is "git commit" which will commit everything in the staging area.

Now you will need to give a commit message describing what that commit changed. There are two ways to do this. The first is to use the commit command above and then a new window will pop up and you can type your message. Alternatively, you can use "git commit -m " and then type the message after the -m. An example is shown below.

![](Images/gitcommit.png)

###### git log
Now that you have gone through the process of committing, you need to track your commits. The easiest way to do this is by using the log functionality. The syntax for this is "git log"
which will pull up the log. An example is shown below.

![](Images/gitlog.PNG)

Here you can see the commit followed by an alphanumeric string. This string is the unique identifier for that commit. If you want to work with that commit in the future, use that string. Additionally, you can see the author, when it was committed and what the commit did.

###### git diff
Now that you have created some commits and viewed the log, it may be beneficial to find what changed between commits. Or more commonly, what your partner changed in their commits. This can be done using the diff command as shown below.

![](Images/gitdiff.PNG)

Shown in the example diff, where the removed text is in red and the new additions are green. You can also see new file additions using this command.

###### git pull
When coding in groups, you will need to keep track of changes made by other people and merge them into your own code. The first step in this process is pulling the code down to your computer from a repository. Before you pull any code, you need to make sure it is code that you want to fold into your system, and that any changes you made are either already saved or they don't matter.

If you want to save your code, refer to git stash as a way to temporarily store your changes. If there are changes that you don't want, refer to the git reset section on how to erase these changes. In either case, once you have decided your repository is ready to fold in some new information, you will use the "git pull" command. Note that this pulls from the online repository that you are connected to by default. If you want to pull from elsewhere, you will need to specify.

Here is an example of me pulling an update from GitHub:

![](Images/gitpull.png)

###### git push
Once you have made changes in your local repository, you can push this changes up to GitHub so that your partner can see your changes and so that if your laptop crashes, you have a backup of your code. As a reminder, git push comes after you have added a new commit. If you have not added a new commit, then you won't be able to push anything.

First, you should make sure that your local branch is up to date, this is done through the git pull command shown above. If your local repository is not up to date, git will not know what to do and you will get an error. After you have checked that your local repository is up to date, you will use the command "git push" and if you want a destination after it. This destination will be useful if you are working with branches as described below. For now, here is a screenshot depicting a successful push.

![](Images/gitpush.png)

###### git branch
Git provides a feature that is useful for adding new features to code called a branch. If you are working on part of a project that has many disjoint parts, it may be useful to work on them separately and then merge them all together as they are completed. While this may be more useful as you work with larger projects, the concept is still worthwhile to go over. You can think of a branch as a separate sequence of commits that you will later merge back into your main master branch.

To begin, let me show you how to list out the branches. You can do this by typing "git branch" which will display all the current branches in your repository. An example is shown below:

![](Images/gitbranch1.png)

In this example above, I use git branch to display the list of current branches. If I want to create a new branch however, you need to be aware of 1 thing. The new branch I am creating will be a copy of the source branch, so if you want to modify your main program, make sure you are on the master branch when you create your new branch. In the example above, I use "git branch branchname" to create a new branch that is a copy of whatever branch I was on to begin this. This branch is denoted by green text. Now that you know what a branch is, I will describe how to change branches below using git checkout.

###### git checkout
Git checkout is the method by which a git user can select which branch they want to work on. The syntax is quite simplistic, as all you need to do is "git checkout branchname". Before you switch however, you need to make sure that your working directory is clean and that you don't have anything in your staging area that isn't committed. If you do not do this, git cannot switch and you shall get an error.

![](Images/gitcheckout.png)

###### git reset
Now I get to come to the fun part of git. What happens when you make a mistake? Luckily, git provides three options for erasing your mistakes. These three options are all options for the git reset command. They are the hard, soft, and mixed. I will cover mixed and hard reset here as I find them the most useful.

First I will cover the mixed reset. This reset is useful because it will modify anything that we have added, but not yet committed yet, while leaving the local files the same. An example of this is if I stage a file but later change my mind about adding it this commit I can use the reset. If I type “git reset HEAD” git will reset everything in the staging area to a specific commit. This can also be used to wipe out local commits that haven’t been pushed yet.

The other type of reset is useful whenever you have really messed up and need to start from a point where you know your code worked. Be careful before you execute this command as it will wipe out any modifications to files you have made since that commit. The syntax is similar to the mixed reset. Now I have an example of reset down below, but I need to explain HEAD~1 first. This is a shorthand for the commit immediately before the one I was working on.

![](Images/gitreset.png)

###### git blame
Ever been in a situation with a lab partner and you want to know whose fault a particular bug is? Luckily git thought ahead and there is a built in mechanism for assigning blame. This tool, called git blame, will go through a file and show who modified each line. An example of git blame is shown below. Additionally, on the far left, git blame will tell you the last commit that changed that line.

![](Images/gitblame.png)

###### git stash
The final git feature that I will talk about is the git stash. Git stash is useful if you want to make a commit, but there is some file or change that is preventing you from committing, and you really care about that file or change. Git stash is a temporary storage area that you can write to and read from as you want. For more information, consult git documentation.
