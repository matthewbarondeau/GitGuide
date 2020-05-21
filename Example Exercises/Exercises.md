## Practice Exercises
This section shall describe additional practices and resources available if you want to explore git more.

### Basic Git Exercises

#### Exercise 1
In this exercise, you will learn how to clone and modify a repository individually. First, create a repository using GitHub. Once you have created the repository, clone it to your machine. Inside this repository, make a change to your data and commit the change. Push this change back up to the repository when you are done.

#### Exercise 2
In this exercise, you will use more of the version control aspect of git. Take the repository you created in exercise 1, and add several more commits. Adding around 3 commits will be the most useful. Once you have added these commits, pull up the git log. Inside the git log, revert your repository to the initial state before you added those new commits. This means clearing the staging area, commit history, and the file changes.

#### Exercise 3
In this exercise, you will focus on the collaborative functionality inherent in Git. Add a friend onto your Exercise 1 repository as a collaborator. Then, have them make a commit and push this commit up to GitHub or GitLab. Your job is then to pull their changes onto your computer without cloning the entire repository again.

### Intermediate Git Exercises

#### Exercise 1
In this exercise, you will work with branches. With your repository from the basic exercises, you will create a branch locally. Use Git Branch and Git checkout to switch to this branch. Make a change and add a commit on this branch. Now the really cool part. Switch back to your master branch and notice that the files in your directory no longer reflect the change on the branch. Cool stuff right?

#### Exercise 2
In this exercise, you will merge a branch into the master. Use your repository from the first exercise and switch to your branch. In this branch, add a couple of commits. This is coolest in exercise 3 if you have several commits. After you have added your changes in the branch, go back to the master and merge this branch in. If there is a merge conflict, try to resolve it. We will cover merge conflicts later on in the advanced section.

#### Exercise 3
In this exercise, we will use git to view changes to your repository and see any existing branches. Normally, we use Git Log to view changes, but it turns out there is a pretty useful graphical interface for this tool. This interface lets you know when branches are split and see how your code has been changing. In this exercise, you need to be on git Bash or in a terminal instance. Using your repository with the merged branch, pull up the graphical git log and see how the branch merges in.

### Advanced Git Exercises

#### Exercise 1
This exercise shall cover merge conflicts. You will need a partner for this exercise. You both need to have the same starting code. Clone the code onto the computers and make different commits and different changes. Both of you should push this code to your repository and you will have to handle the merge conflict.

#### Exercise 2
This exercise shall cover git blame. This fantastic tool is used whenever the code isn't working and you need someone to blame. Go to a project and have you and your partner edit a file and push it back to the GitHub repository. On your computer, run git blame and find out who did the most work on the project by the number of lines. See how great it is!?
