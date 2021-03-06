## Using Git

### Creating and Initializing a git repository
To start using git, we need to setup a git repository. The first step, is lets make a repository on GitHub itself. To do this in EE319k, you can accept the link that the TAs send out for the GitHub classroom. For the sake of completeness however, I will walk you through how to setup your own repository.

When you first open up GitHub, go to the top left of your screen. There will be a small green box that says "new". Click this box. A new window will pop up with options for the repository. You are required to select a repository name, what you want the repository to be called, and choose if the repository is public or private. A public repository can be seen by anyone coming to your GitHub page, so it is best to not put class projects in a public repository. Private repositories means that only you and people you select can make changes to this repository.

Once you have decided on a name and type of repository, select create repository to create a new blank repository. The next step in our process is to connect this remote repository with a local directory on your computer. There are two ways to do this which are discussed below.

#### git clone
The first idea covered here is cloning. That is, making a local copy of a repository that is stored up on GitHub or GitLab. To start, you need to have a repository on GitHub or GitLab, and grab the HTTPS link. You need this link so that you can safely copy the code onto your machine. An example of where to find the https link is shown below.

<p align="center">
  <img src="../Images/https.png"
</p>

Once you have the HTTPS link, its time to pick a location locally that you want to put the repository. In the example below, I navigate to the folder I want to put the repository. I then type "git clone" followed by the https link described above. In this example, I am just cloning the repository that contains my git guide.

<p align="center">
  <img src="../Images/GitClone.png"
</p>

In this way, I can clone an existing repository to a local directory. This can be useful when there is existing code in a repository, but if you have local code or a project that you wish to be associated with a repository, such as in EE319k, the second approach would most likely be to your benefit.

#### git init
The concept of making a local directory a git repository and then pushing it to a hosting platform like GitHub and GitLab is covered here. The first step, is to navigate to the directory that contains the files and folders you want to be hosted. Then, type the command "git init" which will initialize git for the given directory. Once you have initialized the repository, you will need to perform a commit of all the files you want to push up to GitHub or GitLab. The commit process is covered in more depth down below, so if you have never performed a commit, I encourage you to keep reading down to further your understanding.

<p align="center">
  <img src="../Images/gitinit.png"
</p>

Once you know how to perform a commit, select the files that you want to push up and commit them. It is normally good form to have the first commit of your files to be called "Initial Commit". Once you have your first commit, you will need to specify where the remote repository should be. Otherwise, how will git know where to push files? To specify this remote location, the command is "git remote add origin https" where the https is the HTTPS link for your repository.

<p align="center">
  <img src="../Images/remotecommit.png"
</p>

Once you have set the remote location as shown above, it is time to push your files up to the GitHub or GitLab. To do this, you will type "git push -u origin master". This pushes upstream to the remote repository labeled origin and on the master branch.

<p align="center">
  <img src="../Images/pushoriginmaster.png"
</p>

### Creating a Commit

#### git status
The power of git is that you can track changes in code over time. One key aspect to this, is being able to see what in the code has changed since the last commit. So, lets examine how you would see what has changed. First, let me explain the concept of tracking. Git only keeps track of things that you have told it are important. Otherwise, it doesn't care about the other files, it just says that they are untracked. A file starts being tracked anytime you add it to a commit. Anyway, that blurb will be important later.

For now, lets just assume that everything in the repository is tracked. That is, you told git that you care about all the files. To figure out the status of the files that you are tracking, type "git status". An example git status is shown below. Let me walk you through it.

<p align="center">
  <img src="../Images/gitstatus.png"
</p>

In this window, I see that there are some files listed. If I do a "ls" we can see that these are not all the files in the directory. Rather, these are the files that have been modified since the last commit. Keep these files in mind as these are the files we can later add to a commit. Anytime you want to see what has changed, simply do a "git status".

#### git add
Once you have cloned the repository, you can create your files or move them into this repository. At this point however, git is not tracking them. To tell git to begin tracking files, I will use the "git add filename" command. This command will add any file I name to the staging area that I mentioned earlier. If I want to add every file in the repository, I can use "git add ."

An example of git add is shown below:
<p align="center">
  <img src="../Images/gitadd.png"
</p>

Notice how the text turned green. The green text indicates that the file has been 'staged'. All files that are currently staged will be added to the next commit. You can remove any file from the staging area using the "git reset" command.

#### git reset
Now I get to come to the fun part of git. What happens when you make a mistake? Luckily, git provides three options for erasing your mistakes. These three options are all options for the git reset command. They are the hard, soft, and mixed. I will cover mixed and hard reset here as I find them the most useful.

First I will cover the soft reset. This reset is useful because it will modify anything that we have added, but not yet committed yet, while leaving the local files the same. An example of this is if I stage a file but later change my mind about adding it this commit I can use the reset. If I type “git reset” git will reset everything in the staging area to my most recent commit.

<p align="center">
  <img src="../Images/git_reset.png"
</p>

The other type of reset is useful whenever you have really messed up and need to start from a point where you know your code worked. Be careful before you execute this command as it will wipe out any modifications to files you have made since that commit. The syntax is similar to the mixed reset. Now I have an example of reset down below, but I need to explain HEAD. This is a shorthand for the most recent commit. By saying "git reset --hard HEAD", I am removing all changes to my file since the last commit.

<p align="center">
  <img src="../Images/reset_hard.png"
</p>

#### git commit
Alright, now we have finally reached the commit. Once we have added an item into the staging area using git add, we need to permanently save our changes. This is the commit process. The syntax is "git commit" which will commit everything in the staging area.

Now you will need to give a commit message describing what that commit changed. There are two ways to do this. The first is to use the commit command above and then a new window will pop up and you can type your message. Alternatively, you can use "git commit -m " and then type the message after the -m. An example is shown below.

<p align="center">
  <img src="../Images/git_commit.png"
</p>

### Keeping track of your commits

#### git log
So there are two options for seeing what your previous commits were. Once the commits are pushed up to GitHub or GitLab, you can use the GUI to figure out what the commits each did and what lines of code they change. Alternatively, you can use the log functionality built directly into git bash. To pull up the log, the command is "git log", and an example is shown below. One important thing to note before you pull up the log: press the 'q' key to quit out of the log.

<p align="center">
  <img src="../Images/git_log.png"
</p>

Here you can see the commit followed by an alphanumeric string. This string is the unique identifier for that commit. If you want to work with that commit in the future, use that string. For example, if you want to reset to a particular commit, you can use "git commit --hard e35c936" to reset to that particular commit.

#### git diff
Now that you have created some commits and viewed the log, it may be beneficial to find what changed between commits. Or more commonly, what your partner changed in their commits. To view the difference, the command is "git diff" if you want to see all changes. You can also use "git diff filename" to see the changes in one particular file. Shown below is an example diff, where the removed text is in red and the new additions are green. You can also see new file additions using this command.

<p align="center">
  <img src="../Images/gitdiff.png"
</p>

### Synchronizing between computers

#### git pull
When coding in groups, you will need to keep track of changes made by other people and merge them into your own code. The first step in this process is pulling the code down to your computer from a repository. Before you pull any code, you need to make sure it is code that you want to fold into your system, and that any changes you made are either already saved or they don't matter.

If you want to save your code, you can either create a commit or use a stash functionality not covered in this guide. If there are changes that you don't want, refer to the git reset section on how to erase these changes. In either case, once you have decided your repository is ready to fold in some new information, you will use the "git pull" command. Note that this pulls from the online repository that you are connected to by default. If you want to pull from elsewhere, you will need to specify.

Here is an example of me pulling an update from GitHub:

<p align="center">
  <img src="../Images/git_pull.png"
</p>

In this example, the green + symbols incidate the number of lines added to that file. Similarly, the red - indicate the number of lines deleted from those files. Anything that goes from 0 to some number of bytes indicates a file that was created in the commits that you pulled. Note that pulling is different than cloning because in a pull, there is the assumption that the repository is already set up and only has to have a few files updated in order to match the online version.


#### git push
Once you have made changes in your local repository, you can push this changes up to GitHub so that your partner can see your changes and so that if your laptop crashes, you have a backup of your code. As a reminder, git push comes after you have added a new commit. If you have not added a new commit, then you won't be able to push anything.

First, you should make sure that your local branch is up to date, this is done through the git pull command shown above. If your local repository is not up to date, git will not know what to do and you will get an error. After you have checked that your local repository is up to date, you will use the command "git push" and if you want a destination after it. This destination will be useful if you are working with branches as described below. Shown below is a screenshot of git push.

<p align="center">
  <img src="../Images/gitpush.png"
</p>
