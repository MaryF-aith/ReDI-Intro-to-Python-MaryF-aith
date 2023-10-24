# Homework Instructions

## Pre Requisites

- You need a GitHub account and have your credentials ready.
- Complete the steps which were defined in "Python Tool Setup & Installation" https://github.com/neslihankeskin/ReDI-Intro-to-Python/blob/main/1-Intro-to-Python/Install_Python.md. In case you face any issues, write me your issue via Slack message with the screenshot and the step number that you are stuck, and only complete Step 0 & 1.
- Create Git Personal Access Tokens (Classic) [https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic) Do not lose your token this is your password, save it somewhere you won't be able to monitor in this screen again.


## Additional Task
- Start Udacity free course about [Git essential](https://www.udacity.com/course/version-control-with-git--ud123), your deadline is 06.11.2023.



## Step 0 - Fork the Repo and rename it

Open [Redi-Intro-to-Python](https://github.com/neslihankeskin/ReDI-Intro-to-Python)
and sign into your GitHub account.

On the GitHub page for this project, click on the ![fork](../images/fork.png)-button to prepare your own copy 
to store your changes afterwards. 

![fork](../images/1-fork.png)

Update the name by adding your name as a prefix and press "Create fork".

![Create fork](../images/2-fork.png)

Now you 'own' a copy of 'Redi-Intro-to-Python' in your GitHub as 'YourName-Redi-Intro-to-Python'. Go to your Github account and find this repository. As shown below screenshot, click to green code button and select HTTPS copy the URL link.
Henceforth, you will use your copy's URL to check out the code.

![Obtain GitHub URL](../images/3-clone.png)

Watch this demo: https://www.youtube.com/watch?v=XTolZqmZq6s

For a better understanding of Fork and Clone a Repo watch this video: https://www.youtube.com/watch?v=YoGli76EPkU

## Step 1 - Google Colab
### Open the Homework file
[https://colab.research.google.com/?hl=en](https://colab.research.google.com/?hl=en)

There you can open the menu "file/open notebook". In the pop-up window first select the "GitHub" tab. 
second, you need to paste the URL of the repo you copied under Enter a GitHub URL. Third, make sure you selected the  'Yourname-ReDi-Intro-to-Python' repository and then in the drop-down menu and click on the 
"2-Python-Tools/Homework1-Google_Colab.ipynb" jupyter notebook. Jupyter notebooks have the file extension '.ipynb'
![colab](../images/4-colab.png)

Now you can edit the Page content, and execute your answers.
### Save the homework to GitHub
Once you are done with the homework, select the "File/Save a copy in GitHub" menu item.
You can keep most presets, but please enter something meaningful as a "Commit message", as this will help you later to 
understand the goal of the change. Press "OK"  
![save to GitHub](../images/4.1-save.png)
This will create a new version of the file in your copy of the GitHub project. 
### Alternatively, clone the entire repository to Google Colab
On Colab create a new Notebook, run this command with your URL link. ``!git clone https://github.com/[YourGithubName]/[YourRepoName].git``. On the left side you will see the folders and the files on this repository and you can select any file that you want to edit.
![clone](../images/4.2-clone.png)

If not clear watch this video: https://www.youtube.com/watch?v=q0I4CzpBATk

## Step 2 - Jupyter Lab

### Step 2.1 Clone Github repo
Now, you will clone the repo that you forked previously. Note: We practised cloning the repository Redi-Intro-to-Python. However, you do not have permission to push changes for that repo, so that you should clone one of your own repositories to exercise git commands.
Go to Windows Terminal, and make sure that you opened Ubuntu shell
You will see ```(base) root@desktopname:~$```
Run ```git clone https://github.com/[YourGithubName]/[YourRepoName].git ``` for example ```git clone https://github.com/neslihankeskin/ReDI-Intro-to-Python.git``` please replace the link with your own repository which you forked.
This will create a local version of this repository on your computer. In the same way, you can clone any git repository by changing the address.
Run ```ls```. This will list all files and directories on your computer and you should now see a new folder called "Yourname-ReDI-Intro-to-Python".
Run ```cd Yourname-ReDI-Intro-to-Python```. This will show you the files in this directory.
### Step 2.2 Run JupyterLab
On Windows Terminal, you should see ```(base) root@desktopname:~/Yourname-ReDI-Intro-to-Python$``` now activate your environment.
Run ``conda activate intro-to-python`` now you should see ```(intro-to-python) root@desktopname:~/Yourname-ReDI-Intro-to-Python$```
Run ``jupyter lab``. Ctrl + Click on the link to start with ``http://localhost...``` This will launch JupyterLab, and it will redirect you to your default browser. You can now work with notebooks (".ipynb" format) in JupyterLab. Please find and open the Homework1-JupyterLab.ipynb file on the left side under file browser under 2-Python-Tools folder and enter your answers on this file and execute your answers. 

Note: A Jupyter notebook consists of cells. The two main types of cells you will use are **code cells** and **markdown cells**.
- **Code Cells** are for Python script and if you want to execute the code in a code cell, hit Enter while holding down the Shift key (denoted Shift + Enter). Note that code cells are executed in the order you shift-enter them. That is to say, the ordering of the cells for which you hit Shift + Enter is the order in which the code is executed.
- **Markdown Cells** contain text. The text is written in markdown Hitting Shift + Enter renders the text in the formatting you specify.

Once you are done with the homework save the file on JupyterLab. You saved your updates in your local repository but you will push your changes to your Github repo.
1. Open File/New Launcher ![lab1](../images/6-lab1.png)
2. Select Terminal. ![lab2](../images/6-lab2.png)
3. Push your changes with git commands
    - git add . 
    - git commit -m "your message"
    - git push -u origin main ![lab3](../images/6-lab3.png)

*If it asks you to write your username, write your Github Username, and the password is the token you created under pre-requests.*

Note: **DO NOT CLOSE** your Windows Terminal during your work with JupyterLab.


## Step 3 - VSC
### Step 3.1 Clone Github repo
Skip this step if you have already done Step 2.1, if not Do Step 2.1.
### Step 3.2 Run VSC
On Windows Terminal, you should see ```(base) root@desktopname:~/Yourname-ReDI-Intro-to-Python$```. If not, you can close and open a new Windows terminal and run ```cd Yourname-ReDI-Intro-to-Python```.
Run ``code .`` This will open VSC. Note: it might take some time to install the VS Code Server if you run the command for the first time. 
On VSC, open a new terminal and make sure it is a bash shell. Now activate your environment. Run ``conda activate intro-to-python`` now you should see ```(intro-to-python) root@desktopname:~/Yourname-ReDI-Intro-to-Python$```
On file browser find Homework1-VSC.py follow the questions and write your answers then run the file and see the outcome on the terminal window. Make sure you have Python and Jupyter extensions installed under WSL:UBUNTU-INSTALLED folder in extensions. ![extension](../images/4-ext.png)

If not search for them on the marketplace and click install in WSL:Ubuntu. Now click CTRL+Shift + P and click Python:Select Interpreter then you should select Python defined on conda env see the screenshot. ![interpreter](../images/5-interpreter.png)

Once you are done with the homework run the file and check the results on terminal if it is correct. Pay attention it runs the .py file under Python profile.
![VSC-run](../images/7-VSC-run.png)
Then, on the Bash shell run ```git add .```, ``git commit -m "your message for changes"``, and ``git push -u origin main``.
![VSC-push](../images/8-VSC-push.png)

 *If it asks you to write your username, write your Github Username, and the password is the token you created under pre-requests.* 
 Now if you go back to github page you will see your changes deployed to your repository.






