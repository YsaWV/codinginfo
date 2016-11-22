#Git Workflow for Windows


1. Video for walthrough
  * [GitBash Walkthrough](https://vimeo.com/157763346/e0016ba546)

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

##Commit changes

1. In GitBash, type git status to see what files have been modified since your last commit. 
		
		Note: Make sure you are in the proper directory of your repo. To check which directory you are in, type pwd (print working directory). If you are not in the proper directory, use cd to change to the directory of your repo 

2. In GitBash, type git add [nameOfFileToAdd] where the [nameOfFileToAdd] matches the filename as shown from the previous command. Repeat this step as necessary until all files that you want have been added. To add all files that have been changed at once, type git add .. Now the selected files are staged for commit, but are not committed yet.

3. In GitBash, type git commit -m 'add a message here that tells your future self what changes you made' to add the selected changes to your Git history.

4. To push the changes up to your Github, type git push origin master in GitBash. This will push the changes to the "master" branch of your remote called "origin". You may need to enter your Github credentials at this point. Note that when you type your password, it might appear as a single flashing dot.



##Add a remote

2. Send your pair the Git link to your repository via Slack. This is the same link you used to clone the repository to your local machine. You will need this information to set up remote repositories later.

3. In GitBash, navigate to the repository. Type git remote -v to see what remotes are already associated with the repository. Most repositories have an "origin" remote set up by default.

4. In GitBash, type git remote add [nameOfNewRemote] [pasteLinkToYourPartnersRepositoryHere] then hit enter to add your partner's repository as a remote repository. We recommend naming the [nameOfNewRemote] your partner's name for simplicity.

5. In GitBash, type git remote -v again to verify that the remote was added. If it was successful, you should see "origin" in addition to the name of the remote you just added.
