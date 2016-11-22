# Git Workflow Cheat Sheet for Prep+ Students

You will be using Git and Github extensively in this class. This cheat sheet  outlines the steps you will take to fork and clone the class repositories, as well as the steps for saving/pushing your work to Github when pair programming during class. You will be interacting with Git through the terminal.

If you are working on a Windows machine, use the following links to set up Git on your machine.

1. Video showing how to install Git for Windows
  * [GitBash Walkthrough](https://vimeo.com/157763346/e0016ba546)

2. Reference the Git Workflow for Windows document
  * [Git Workflow for Windows](https://github.com/TelegraphPrep/PrepPlus-Wiki/blob/master/GitWorkflow-Windows.md)

## How to fork and clone repositories

All of the exercises for this class can be found on the Telegraph Prep Github [here](https://github.com/TelegraphPrep). To get the repository onto your local machine, follow these steps:

 **Fork the Repository**
 
1\. On Github's website, navigate to the repository that contains that day's exercises/project.  
2\. Click the "Fork" button near the top right part of the screen.  
3\. In the popup box, select your Github profile to copy the repository from the TelegraphPrep Github profile to your profile.  

 **Clone the Repository**

4\. Once the repository is on your Github profile, navigate to your fork of that repository on Github's website.  
5\. Click the "Copy to clipboard" button to copy the Git link for the repository.  
6\. In your terminal, navigate to the folder you want to copy the repository into.  
7\. In your terminal, type `git clone [pasteTheLinkYouJustCopiedHere]` then hit enter to clone the repository from Github to your local machine.  

**Open the Repository on Your Local Machine**

8\. In your terminal, navigate to the repository.  
9\. View the location of that repository in your finder by typing `open .` into the terminal.  
10\. To open the repository in Sublime, drag the repository folder over the Sublime icon in your Dock (at the bottom of the screen). All of the files within the repository should now be viewable in the sidebar in Sublime.

## How to Save, Commit, and Push Your Work to Github

Save, commit, and push your work frequently when programming. We recommend saving, committing, and pushing your work after each task you complete (e.g., each function you write, each test you pass) and at least every 20 minutes. To get your work from your local machine onto Github, follow these steps:

**Save Your Changes**

1\. Type `command+s` in each file that has changes to save your work.  

**Commit Your Changes**

2\. In your terminal, type `git status` to see what files have been modified since your last commit.  
3\. In your terminal, type `git add [nameOfFileToAdd]` where the [nameOfFileToAdd] matches the filename as shown from the previous command. Repeat this step as necessary until all files that you want have been added. To add all files that have been changed at once, type `git add .`. Now the selected files are staged for commit, but are not committed yet.  
4\. In your terminal, type `git commit -m 'add a message here that tells your future self what changes you made'` to add the selected changes to your Git history.  
5\. To push the changes up to your Github, type `git push origin master` in your terminal. This will push the changes to the "master" branch of your remote called "origin". You may need to enter your Github credentials at this point. Note that when you type your password, it might appear as a single flashing dot.  

## How to Work with Github When Pair Programming

When you're pair programming, two people will be working on one computer - one as the driver and one as the navigator. Ultimately, both people will need that version of the code on their own forks of the repository. For this to work, each pair can only be making changes on **ONE COMPUTER AT A TIME**. In order to set up remotes and push work to multiple repositories, follow these steps:

1\. Each of you should fork and clone the repository to their local machine. 

2\. Each of you will need to add each other as collaborators to your online repos so that they can have *write access* to your repository and push changes up to your branch. 


You can do this by going to the settings tab in the upper right hand corner of the repository options tab. On the settings page, click the collaborators tab.

![](http://i.giphy.com/PHwFtSanZI6MU.gif)

Then, each of you add one another as a collaborator by typing your partners github name into the input bar in the Collaborators section. Make sure that they have write access!

![](http://i.giphy.com/iFNbpjj2XhzX2.gif)


**Add a Remote**

3\. Send your pair the Git link to your repository via Slack. This is the same link you used to clone the repository to your local machine. You will need this information to set up remote repositories later.  
4\. In your terminal, navigate to the repository. Type `git remote -v` to see what remotes are already associated with the repository. Most repositories have an "origin" remote set up by default.  
5\. In your terminal, type `git remote add [nameOfNewRemote] [pasteLinkToYourPartnersRepositoryHere]` then hit enter to add your partner's repository as a remote repository. We recommend naming the [nameOfNewRemote] your partner's name for simplicity.  
6\. In your terminal, type `git remote -v` again to verify that the remote was added. If it was successful, you should see "origin" in addition to the name of the remote you just added.

**Driver/Navigator Workflow**

7\. Together, decide which computer you will work on first and who will be the driver or navigator first, then **CLOSE THE NAVIGATOR'S COMPUTER**. Note: If you make changes on both computers simultaneously, you will have merge conflicts later and you really, really want to avoid having merge conflicts right now.  
8\. Commit your work frequently, after you complete a task and at least every 20 minutes.  
9\. Every 20 minutes you should be switching driver/navigator roles.  
10\. When it is time to switch roles, commit all of your latest changes, even if you're in the middle of a task. See the [PrepPlus Wiki](https://github.com/TelegraphPrep/PrepPlus-Wiki) for details on how to do that.  

**Pushing to Multiple Remotes**

11\. Push to the "origin" remote like normal by typing `git push origin master` to push the changes to the "master" branch of your remote called "origin". You may need to enter your Github credentials at this point.  
12\. Push to the [nameOfNewRemote] remote by typing `git push [nameOfNewRemote] master` to push the changes to the "master" branch of your remote called [nameOfNewRemote]. You may need to enter your Github credentials at this point.  

**Pulling Changes from Github**

13\. When you switch driver/navigator roles, after you push your work to both remotes, switch computers as well. The changes are on Github, but are not yet on the new computer.  
14\. To get the changes from Github, type `git pull origin master` to pull down changes from the "master" branch of your remote called "origin". Now the version of the repository on your local machine matches the version that is on Github. Note: you will get merge conflicts at this point if you were changing files on both computers simultaneously.  

