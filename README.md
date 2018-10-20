# GitHub Tutorial

_by Zhiyuan Chen_

---
## Git vs. GitHub

* Git  
    * A version control system that tracks changes made to folders or files.
    * Shows users a list of changes with a message that the user gave to git  
      When users request for the change history. 
* GitHub 
    * Using git's system of version control and adding in visuals that    
      help people easily see changes. 
    * This online website allows collaboration between many programmers   
      because programmers can access each other's code and make changes  
      that the original creator might approve.

---
## Initial Setup
In order to interact with the Github system, creating a Github account is essential.  
**Note : All of this is subject to change by Github. This tutorial is made in October 2018**
1. Go on [**_Github_**](https://github.com) <~~ Hover your mouse over & click to get access to Github directly.
2. Go to the upper right corner and click _**Sign up**_
3. For **Username**, give yourself a name that you can remember.
      * If your username is taken, you might have to alter it until Github approves.
4. Remember to use your school email or your own for **_Email address_** 
5. For **_Password_**, give yourself a password such as ID Number
6. Press the green **_Create an account_** button
7. Choose the free plan or spend $7 for the paid plan
8. As you approach step 3 on Github, answer the questions about your experience
9. **You have successfully created a Github account!!**  

## SSH Key Setup
1. Go on [**_c9.io_**](https://c9.io) to get the SSH key
2. Create new account if you do not have one or sign in with existing account
      *  If you create your own account, you will likely need a credit card.
3. Click on the settings icon on the upper right
4. On the very left side bar, you should be on **Settings**, click **_SSH Keys_**
5. Copy the second SSH Key 
6. Go back to your Github page
7. Click on personal icon and go to **_Settings_**
8. Go to **_SSH and GPG keys_** 
9. Click the button "**_New SSH key_**"
10. Name the title "_**cloud9**_"
10. Paste your copied SSH Key with command v (Mac) or control v (windows)
10. **You have successfully link cloud9 with Github!!**

---
## Repository Setup
Since you have your Github account **NOW**, follow the steps below to create a repo  
**_Repository_** : this is where you can save and store your local files onto an online remote.
1. On Github, click on the little downwards triangle next to user icon
2. Select "_**Your repositories**_"
3. Click the green "**New**" button
4. Give your repository a name
5. Choose if you want to show it to the public or keep it private
6. **_You have successfully created a github repository_**
7. You will be redirected to a page with different lines of code
8. From **Github** : Copy few lines of code similar to the ones below from your repo
```
git remote add origin git@github.com:git-us/git-tutorial-demo.git
git push -u origin master

```
9. Go back to cloud9
      * If you do not have a workspace then follow these steps:
      * Click "**_Create a new workspace_**"
      * Give the workspace a name and optional description
      * Choose a template (for this tutorial, we are using **_Blank_**)
10. Open up your workspace if you haven't
11. You will see a **terminal** called **_Bash_**
12. A **README.md** will be opened.
13. On the left side bar, a folder will be named after your workspace's name  
      ```
      Note that this folder cannot be a repository because it is our main workspace 
      folder that holds every other repositories and files. 
      ```
14. On the left side bar, right click and choose **New Folder**
15. Give it the name of your Github repository
16. Put your cursor over README.md file and drag it into the new folder. 
17. On the terminal **Bash**, type :  
      ```
      cd folder_name
      git init
      ```
      For folder_name, replace that with your repository's name  
      My command would then be **cd git-tutorial-demo**
18. You are now starting a git project
      ```
      :~/workspace/git-tutorial-demo (master) $ 
      ```
      You should see something like the line above in the terminal
19. Now open the README.md file editor by typing this into terminal :
      ```
      c9 README.md
      ```
      remember to press **ENTER** after the command  
      md stands for markdown and you can edit the README.md in any way you like.
20. Remember to save the edited README.   
      `
      click inside the README and press control s (Windows) or command s (Mac)
      `
21. Click on to the terminal and type one of these comamnds :  
      ```
      git add README.md       
      git add .
      ```
22. Now following the previous command, type :  
      ```
      git commit -m "Edit README"
      ```
23.
      Paste the copied commands from before (**STEP 8**)
      ```
      git remote add origin git@github.com:git-us/git-tutorial-demo.git
      git push -u origin master
      ```
23. Go on to your Github repository page and you should see your files **:)**
---
## Workflow & Commands



---
## Rolling Back Changes
