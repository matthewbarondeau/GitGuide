#### Linux Navigation
This section shall detail how to navigate the git bash terminal. The git bash terminal is based on the Linux terminal so the commands for navigation are the same. Therefore, if you already know the Linux terminal, you can skip this section.

###### Finding out where you are
We will first start by learning how to navigate through this shell. To start, we should find out where we are. This can be done by typing “ls” into the window and pressing enter.  This should bring up all the directories or folders inside of our current folder. It should look something like this:

![](Images/ls.png)

###### Changing Directories
Now that you have listed out the folders that you have access to, it is important to be able to navigate between them. If we want to change to a folder, we can use the “cd” command. The cd command has three main use cases. Additionally I will demonstrate how these instructions can be used:

1. You can type “cd ..” to go back one folder.
2. The cd C:Work/445L/445L-Lab5/ command will change my current folder to the 445L-Lab5.
3.  If the folder I want to go to is inside of my current folder I can say “cd 445L-Lab5” to change.

![](Images/cd.png)
###### Creating Directories
Finally, you will want to create a new folder to work with. Navigate to the location that you want to work with and type “mkdir foldername”. This will create a new folder that you can navigate into and work with. Below is an example of a directory before and after a mkdir instruction.

![](Images/mkdir.png)

###### Removing Directories
In the event that you create a folder or document that you want to remove, there is a handy command to delete them. Of course, you could always navigate to the file directory and delete it normally, but this is cooler. To remove a file, type rm followed by the file name. An example of this is here:

![](Images/rm.png)

If you want to remove a folder, you can use "rm -r dirname" to remove a full directory. Anything that is write protected you have to manually select. So as usual, be careful when deleting stuff.
