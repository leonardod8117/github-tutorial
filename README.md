# GitHub Tutorial
 
_by Leonardo De La Rosa_

---
## Git vs. GitHub
###Git
* Git has "version control", which means it manages multiple versions of a file   
  by allowing you to take "snapshots" of code.  

* Also, Git does not require Github.  

###Github 
* Github requires Git because it serves to store code generated in Git in the cloud.

* It visually tracks changes so when ever changes are made in a file you can view those  
  changes in Github.  

* Files in Github are easily collaborated because they are public so anyone can view them  
  and suggest or make changes to them. 


---
## Initial Setup
* To begin using Git and Github you should start by creating a Github account.  
 * Go to [Github.com](github.com) and sign up for free.  

* After signing up for Github you need to link your Github account with your Intergrated  
  Development Environment or **IDE** from the platform you are using.  
    * In github, click on your account icon in the top right hand corner.
    * Go to settings and click on _SSH Keys_ then go to the platform the **IDE** is on   
    and go to settings.   
    * Obtain the _SSH key_ in the settings and copy it.
    * Then return to github, click on add _SSH key_ and paste.  

* After connecting your Github account and your IDE, you should open your IDE and see  
 the following: `ssh -T git@github.com(yes/no)`  
 * Type in yes and you have successfully connected your IDE with your Github. 

* In order to receive credit for your work, you must use the command `git config --global user.name  
 "first name last name"` and `git config --global user.email "email"`. When you enter these commands individually, they should look like this:  
 * `git config --global user.name "Leonardo De La Rosa"`  
    `git config --global user.email "anderosa8@gmail.com"` 
   
  


---
## Repository Setup
* To begin using Git you must do the following:  
 * Go to your directory(folder) of files.  
 * Intialize Git using the command `git init`, which gives you version control and creates  
   a repository(where files are kept and changes are tracked).

* After you have created a file in a repository and have made changes, you should save it by doing  
  the following:  
 * In the repository the file is located, type in the command `git add {name of file}` to add the file in the  
   repository to the stage.  
 * Then type in the command `git commit -m ""` and write a message between the quotes about the changes  
  you have made in the file. 

* In order to see the repository and the files within it on Github you should do the following:  
 * you must go to Github and click on the plus icon in the top-right hand corner and click on new repository.
 * In the space provided, type the name of your repository in git and then click create repository. 

* You will then be brought to a page where you are given instructions on how to setup a connection between  
  the external repository(remote) in Github with the one in Git and you are provided with an SSH link to the repository.  
  To make the connection you should copy and paste these two commands in git:  
 * `git remote add origin SSH link here`  and  `git push -u origin master`.  

* After doing the previous step, you should refresh your page and be able to see the changes you made in your repository on Github.

---
## Workflow & Commands
### Basic Workflow  
* Whenever you make any changes to a file in a repository on git, you should:  
 *  Use the command `git add file name` to put the file on the stage.
 *  Then type in the command `git status` to see if the file you made  
    changes to is on the stage.  
 * Type the command `git commit -m ""` and write a message regarding   
   the changes you have made in the file.  
 * Type in the command `git push`  
   (Note: you do not have to type in `-u origin master` because  
   when you did so the first time, you were commanding Git to   
   remember the remote you entered previously).  

### Commands
* The Git commands you should know are as follows:
  1. `git init`: initializes git in the directory you are currently in.  
  
  2. `git add file.ext`: adds file to stage to be committed. 
 
  3. `git commit -m "short-specific message"`: takes a 'snapshot' of files  
      on the stage. The message should be short and describe what changes
      were made to the file.  
  4. `git status`: tells you which files were placed on the stage.(It will be green) 
  
  5. `git remote add origin SSH link here`: This creates a connection between a repository in git  
     and an external repository in Github.  
  6. `git push`: sends any changes made in a repository in Git to an external repository you made in Github.  
  
  7. `git help`: this will list commonly used commands in git.  
  
  8. `git log`: use this to see a list of all your past commits. 
  
  9. `git diff`: shows you the difference between your current code and the last 'snapshot' of your code.  

---
## Error Handling  
* If you intialized Git in the wrong directory, don't fear and follow the directions listed here:  
  * Go to the directory you intialized git in and type in `rm -rf .git` and press enter. This should "un-init"  
   git so you can initialize git in the correct directory.  

* To remove a repository in Git you should:  
 *  Be in the directory that the repository is located in.
 *  In this directory, type in the command "rm -rf name of repo" to remove the repo forcefully.  
 
* To remove a repository in Github you should:  
  * Go to the repository's main page on Github. 
  * In the repository's sidebar on the right side, click on settings.
  * Scroll down to **Danger Zone** and click on _Delete this repository_. 
  * Read the warning, type in the name of the repo, and click **I understand the consequences,delete this repository**.  

### Forking & Cloning    
* If you were to accidentally delete a repo in git, you can take a copy of it from github with cloning by:  
 * Going to the main page of the repo in Github.
 * Look for the SSH clone URL below the right side bar and copy it. 
 * Return to git and type in the command `git clone SSH clone URl` in the directory you want to place the repo in.  

* If you want to use someone else's work as the foundation for your work, you can use forking by:  
  * Going to the main page of the repo that you want to use as a starting point and click on fork at  
    the top-right of the page. By forking this repo, you are making a personal copy of it that you can  
    make changes to.  
  * After forking the repo, go to the main page of your personal copy of the repo and copy the SSH clone URL  
    below the right sidebar.  
  * Go to git and type in the command `git clone SSH clone url here` and you now have the forked repo in git.  

* If you wish to offer the changes you made in your personal copy of the forked repo to the owner of the original  
  repo, you must:  
  * Go to the main page of your forked copy of the repo in Github. 
  * Click the green button in the top left of the page, next to the branch button. 
  * A new page will open and you will see a button that reads "create pull request". Click the green button. 
  * You are given the option too write a comment and once you are done, click "create pull request" below the text box. 

  