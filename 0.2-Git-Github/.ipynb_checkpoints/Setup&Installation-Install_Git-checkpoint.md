# Python Tool Setup and Installation- Cont'd


### 3 Git

Git enables us to version control our files and track changes so that we have a nicely structured recorded history and don't need to duplicate files to save different versions in an intransparent way. It also gives us the ability to easily revert to previous versions of files and makes collaboration easier, allowing changes by multiple people to be merged into a common repository.
#### 3.1 Installing Git

Run the following command to install git based on your OS 

**Linux - Ubuntu distribution**
```sudo apt install git-all```

**Linux - Fedora, CentOS, RHEL and other RPM-based distribution**
```sudo dnf install git-all```

**macOS**
```brew install git```

**Windows**

**Install Git in WSL**
**Documentation & Instructions**: [https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-git](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-git)

- Run the following from your bash command line interface (inside Windows Terminal) to install the latest stable Git version:
```sudo apt-get install git```. 


**Alternative**
Download git from [link to download git](https://git-scm.com/downloads)
Install git with the downloaded file 

For more information on how to install git check [here](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) 

#### 3.2 Testing Git Installation

To confirm you have installed git, run the following command on your terminal
- Run ```git --version```.

If it output some numbers which represent the version of git you installed, this confirms git is installed
- You must see ```git version 2.25.1```


**Documentation**: [Git Documentation](https://git-scm.com/doc)

#### 3.3 Register a GitHub Account


- If you don't yet have a GitHub account, sign up [here](https://github.com/).


#### 3.4 Git Config File Setup

- To set up the Git config file, run on your terminal:
```git config --global user.name "<YOUR_NAME>"``` and replace <YOUR_NAME> with your Github Account user name. For example, git config --global user.name "neslihankeskin"

- Then run ```git config --global user.email "<YOUR_EMAIL>"``` and replace <YOUR_EMAIL> with your Github Account email. For example, git config --global user.email "neslihankeskin@gmail.com"

- If you need to edit the Git config, you can use the text editor nano as follows:
```nano ~/.gitconfig```. When you are done, save the changes with CTRL + X  -> Y -> Enter.

#### 3.5 Getting ReDI course repo

- From the bash command line interface in your Windows Terminal or on your terminal for other OS  run: 

```git clone https://github.com/neslihankeskin/ReDI-Intro-to-Python.git```

 This will create a local version of this repository on your computer. In the same way, you can clone any git repository by changing the address. 
 
 **This is needed before we can progress with subsequent steps.**

- DO THE FOLLOWING STEPS AT THE BEGINNING OF EACH LESSON TO GET UP-TO-DATE CONTENT
- Run the command 

```ls``` 

This will list all files and directories in that folder and you should now see a new folder called "hh-dcp-intro-to-computer-science".

- To update your local repository to the most up-to-date status of the remote version, navigate into your repository 

```cd ReDI-Intro-to-Python```

 **Note:** you can use the tap key to autocomplete the directory name.
 
 Then 
 
  ```git pull```
  
You should run this command at the start of every lesson to have **up-to-date content**.

#### 3.6 Homework

**More information on Git**
- Udacity has a very good free course about Git essentials [here](https://www.udacity.com/course/version-control-with-git--ud123). In general, we would strongly advise to use Git for version control for your future coding projects. 
