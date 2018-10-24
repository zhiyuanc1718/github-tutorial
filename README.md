# GitHub Tutorial

_by Zhiyuan Chen_

---
## Git vs. GitHub
* Git  
    > A version control system that tracks changes made to folders or files.  
    > Shows users a list of changes with a message that the user gave to git      
    > when users request for the change history.   
* GitHub 
    > Github uses git's system of version control and adding in visuals that help people easily see changes.   
    > This online website allows collaboration between many programmers because programmers can access 
    > each other's code and make changes that the original creator might approve. 

---
## Initial Setup
In order to interact with the Github system, creating a Github account is essential.  
**Note : All of this is subject to change by Github. This tutorial is made in October 2018**
1. Go on [**_Github_**](https://github.com) <~~ Hover your mouse over & click to get access to Github directly.
2. Go to the upper right corner and click **Sign up**
3. For **Username**, give yourself a name that you can remember.
      > If your username is taken, you might have to alter it until Github approves.
4. Remember to use your school email or your own for **Email address** 
5. For **Password**, give yourself a password such as ID Number
6. Press the _green_ **Create an account** button
7. Choose the free plan or spend $7 for the paid plan
8. As you approach step 3 on Github, answer the questions about your experience
      > You have successfully created a Github account!!

## SSH Key Setup
1. Go on [**_c9.io_**](https://c9.io) to get the SSH key
      > The SSH key is used as an automatic sign-in process  
      > This links c9 to Github and will not require you to sign in with your password  
      > That is the downside of using HTTPS which requires your password for every change that is sent to github.  
2. Create new account if you do not have one or sign in with existing account
      > If you create your own account, you will likely need a credit card.
3. Click on the settings icon on the upper right
4. On the very left side bar, you should be on **Settings**, click **SSH Keys**
5. Copy the second SSH Key 
6. Go back to your Github page
7. Click on personal icon and go to **Settings**
8. Go to **SSH and GPG keys** 
9. Click the button "**New SSH key**"
10. Name the title "**cloud9**"
11. Paste your copied SSH Key with command v (Mac) or control v (Windows)
      > You have successfully link cloud9 with Github!!

---
## Repository Setup
Since you have your Github account **NOW**, follow the steps below to create a repo  
**_Repository_** : this is where you can save and store your local files onto an online remote.
1. On Github, click on the little downwards triangle next to user icon
2. Select "**Your repositories**"
3. Click the _green_ "**New**" button
4. Give your repository a name
5. Choose if you want to show it to the public or keep it private and Create Repository.
      > With that, You have successfully created a Github repository
6. You will be redirected to a page with different lines of code
7. From **Github** : Copy two lines of git commands similar to these below  
      ```
      git remote add origin git@github.com:git-us/git-tutorial-demo.git
      git push -u origin master
      ```
8. Go back to cloud9  
9. **_ONLY_** If you do not have a c9 workspace then follow these steps:
      > Click "_Create a new workspace_"  
      > Give the workspace a name and optional description  
      > Choose a template (for this tutorial, we are using "_Blank_")
10. Open up your workspace if you haven't
11. You will see a _terminal_ called **_Bash_**  
      If terminal is not opened or you do not see one then :  
      > Press **`alt` and `t`** would open a terminal or ...  
      > Locate a circle with a plus sign, click it and choose New Terminal
12. A README.md will be opened and created for your new workspace.
      > If this is not a new workspace then type : **`touch README.md`** in terminal after _$_  
      > This command will be explained on the next section
13. On the left side bar, a folder will be named after your workspace's name  
      > Note that this folder cannot be a repository because it is our main workspace   
      > folder that holds every other repositories and files. 
14. On the left side bar, right click and choose **New Folder**
15. Give it the name of your Github repository
16. Put your cursor over README.md file and drag it into the new folder. 
17. On the terminal **Bash**, type :  
      ```
      cd folder_name
      git init
      ```
      > For folder_name, replace that with your repository's name  
      > My command would then be **`cd git-tutorial-demo`**
18. You are now starting a git project
      ```
      :~/workspace/git-tutorial-demo (master) $ 
      ```
      > You should see something like the line above in the terminal
19. Now open the README.md file editor by typing this into terminal :
      ```
      c9 README.md
      ```
      > remember to press `ENTER` after the command      
      > md stands for markdown and you can edit the README.md in any way you like.
20. Remember to save the edited README.   
      > click inside the README and press control s (Windows) or command s (Mac)
21. Click on to the terminal and type one of these comamnds :  
      ```
      git add README.md       
      git add .
      ```
22. Now following the previous command, type :  
      ```
      git commit -m "Edit README"
      ```
23. Paste the copied commands into the terminal from before (**STEP 8**)    
      ```
      git remote add origin git@github.com:git-us/git-tutorial-demo.git  
      git push -u origin master`
      ```
      > Magic does not happen unless you confirmed by pressing `ENTER`
24. Go on to your Github repository page and you should see your files uploaded
      > You have completed the setup for the repository !!  
      > It is time to understand all those git commands !!

---
## Workflow & Commands
#### Command Line commands (Terminal Use)
> This is just a list of commands that would make coding in the terminal faster  
> Note that these commands might come handy but not necessary in working with git

|Basic Commands|Syntax (Format)|Purpose and Use
|--------------|------|-------|
|cd|`cd [folder_name]`|move your current path to a different path (change of location in file system)
|mkdir|`mkdir [name]`|creates a new folder that holds folders/files
|rmdir|`rmdir [name]`|deletes an empty folder or directory if name exist
|touch|`touch [file_name`]|creates a new file in the current directory
|rm|`rm [file_name]`|deletes a file given name exist
|mv (1)|`mv [old_name] [new_name]`|renames a file or folder
|mv (2)|`mv [name] [existing_name]`|moves one file/folder into another
|c9|`c9 [file_name]`|quick way to open a file  
|ls|`ls -` `a` `l` `t`| list out files. a for hidden, l for long format, t for chronological order
|pwd| `pwd`| unnecessary if you work in the c9 terminal. it tells you the current directory you are in

#### Git commands (Necessary)
> This is just a chart of the commands, see below for further explanation  

|Command|Syntax (Format)|Purpose and Use
|--------------|------|-------|
|init|`git init`|Creates a repository and allows the use of git commands.
|status|`git status`|Shows the user which files are on stage and which are not.
|add|`git add [name]`|Adds a file to the stage and prepares the file for commit
|add .|`git add .`|Adds all modified/new files to the stage
|add --all|`git add --all`|Adds all files including renamed/deleted files to the stage
|diff|`git diff`|Shows the difference between last commit and current modified files
|commit|`git commit -m [message]`|Tells git to save all changes and give this change a `message` as reminder
|remote|`git remote add origin [url]`|Links the Github remote to the local repository. This tells git where to upload your files to.
||`git remote -v`|Tells the user where they are uploading files to
|push|`git push -u origin master`|Tells git to send the newest saved changes (commit) to Github
||`git push`|This command can be used once the previous command has been used.
|log|`git log`|Shows the history of commits to the user in order from most recent to oldest

---
#### General Workflow
* Repository Setup
* Editing and saving Files
* Adding to the stage 
> This means to get the files prepared to be saved to file history
* Commiting the file(s)
> This means you are 100% sure that whatever changes you made and added to the stage  
> Is then added to the file history as an update of file(s) for future reference
* Pushing the commit 
> This step is essential for your Github to get access to your new updates on your local folders

_**Use these commands in this order, exceptions to `git status`/`git remote -v`**_ 
1. **`git init`** :    
      > This is extremely essential for any of the other git commands to work    
      > This makes your current folder a git repository and allows you to begin tracking changes  
      
      **NOTE** : DO NOT EVER ATTEMPT TO TYPE THIS COMMAND IN YOUR WORKSPACE FOLDER  
      `:~/workspace $ git init (PLEASE DO NOT DO WHATEVER IS TO THE LEFT)!!!`  
      
      **IF** you ever do that, of course, mistakes can happen, we will have to un-initialize  
      > type **`rm -rf .git`** : this deletes the git repository.   
2. **`git status`** :  
      > A powerful command that tells the programmar which files are edited  
      > **`Green`** = ready to commit while **`Red`** = not included in next commit  
      > Often times if you encounter an issue or error, you might want to use this command  
      
      This command does not interfere with any other command. **FEEL FREE TO USE**!!  
3. Now that you have edited your files, remember to save them   
      (**Forget how?**, refer back to **STEP 20** of Repository Setup)
4. **`git add`** :  
      > Ready to have a file or multiple files to be saved to the commit history?  
      > We need to add them to the stage first with one of the following comannds  

      `git add [file]` : Fair and simple, give it the name of a file   
      `git add .` : This one is a shortcut if you need to add multiple new/edited files to the stage.  
      `git add --all` : This is for all files and even those you gave a new name to.  
5. **`git commit`** :
      > Commiting is the step that says you are ready to save every change you include in the stage

      The syntax is `git commit -m [message]`   
      > notice that your message must include quotation marks  
      > For a good message, make it present tense and specific such as :  
      
      `"Add images to the repository setup section for easier understanding"`
6. **`git remote add origin [url]`** :
      > The `url` input in this command is the SSH url provided from Github  
      > You would not need to use this command if you have went through the steps in the repository setup  
      > In general, this command tells your `git push` command where to push or upload files to.
7. **`git remote -v`** :
      > From previous command, it is important to have the remote link added to the local git repository  
      > By typing this command, if nothing shows up, then you have not connected remote to your local repo  
      > With proper setup, you should see something like below :

      ```bash
      origin  git@github.com:username/repository_name (fetch)
      origin  git@github.com:username/repository_name (push)
      ```
8. **`git push`** :
      > Pushing, as mentioned before is to give your commits to your remote (in this case Github)
      
      The first time you use push in a repo, I recommend using `git push -u origin master`
      > This tells the local to remember that you will be pushing to the `master` branch

      Any other future push, you might use `git push` as a shortcut because git already remembered destination = master.
9. This is the end of the workflow, you might visit Github to check your update.

---
## Rolling Back Changes
If you ever mess up your files or saved something you didn't want to... well undo(s) exist.

* Undo file edit : `git checkout -- [filename]`
> This command can undo a saved file change to what is was previously. 
* Undo git add : `git reset HEAD [filename]`
> This command removes your specified file from the stage. This is called **`unstage`**
* Undo git commit : This is a bit different and you have a few options...  
      1. Remove the commit and keep your files on stage : `git reset --soft HEAD~1`  
      2. Remove the commit and unstage the files as well : `git reset HEAD~1`  
      3. Remove the commit, unstage and undo edits : `git reset --hard HEAD~1`  
* Undo git push : want to remove what you push/upload to Github?  
      `git revert commit_SHA` : to find the SHA a specific code given to each commit, type: `git log`  
> Find the SHA code of the previous commits and to quit the log, press **`q`**  
> You may chain a list of SHA by adding another SHA after the most recent commit  
> This will bring you back 2 commits and so on if you repeat.  

---
## Removing repository on Github/Local
If you somehow what to delete your Github remote... then Follow these Instructions :  

1. Open up your repository on Github
2. Go to the settings of the repository
3. Scroll all the way down to an area called danger zone
4. Click `Delete this repository`
5. Enter the name of the repository in the pop up
6. Well.. there you go. You have deleted your remote

If you want to remove the local repository... then Follow these Instructions as well :

1. Deleting the folder first requires you to be in its parent folder
2. For example you will see in the terminal : `~/workspace/music (master) $ `  
3. This means that you are currently within a folder with parent folder as `workspace`
4. you will then use the following two commands to the right of the shell prompt `$`
```bash
gitus12345:~/workspace/music (master) $ cd ~/workspace
gitus12345:~/workspace $ rm -rf music 
```
And no, you will not type `music` like shown. Replace that with your local repository folder name !!