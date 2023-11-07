# Python Tool Setup and Installation


## Tools Setup

Before we  start programming in python, we need to install the required tools used for running python code. Since python is the major language used for data science, some of the installed tools can also be used for data science projests. **The installation guide is focus on Windows OS**, the steps may be a bit different for MacOS and Linux.  We will cover the setup and installation of the following tools:
- Windows Subsystem for Linux (WSL)
- Windows Terminal
- Git
- Miniconda / Conda & Python
- Visual Studio Code
- JupyterLab

**If you use a Unix based OS(MacOS and Linux), you can skip the installation of Windows Subsystem and Windows Terminal**


### 1 Windows Subsystem for Linux (WSL)

WSL enables us to use a Linux distribution operating system with Linux tools on our Windows machines in a completely integrated manner (no need to dual-boot).
When we install a Linux distribution with WSL, we are installing a new file system, separated from the Windows NTFS C:\ drive.

**Documentation**: [https://docs.microsoft.com/en-us/windows/wsl/](https://docs.microsoft.com/en-us/windows/wsl/)

#### 1.1 Installing WSL

**Documentation & Instructions**: [https://docs.microsoft.com/en-us/windows/wsl/install](https://docs.microsoft.com/en-us/windows/wsl/install)

- Search for Command Prompt(PowerSheell) on your computer Open PowerShell
- Right click on it and run as an administrator 
- Run the following command in your command prompt 

```wsl --install -d Ubuntu``` 

This will install WSL together with an Ubuntu distribution on your computer. You may need to reboot your to make the installation take effect.

- Once you have installed WSL, you should now have Ubuntu in your Windows Start Menu. Open Ubuntu from the Windows start menu (if it has not opened automatically after installation). We can also pin Ubuntu to your Windows taskbar for easy accessibility in the future. 

**Note: If you can't find Ubuntu in your Windows start Menu after installation, please restart your computer** 

- You will now be prompted to create a user account and password for your newly installed Linux distribution. This account will be considered the Linux administrator, with the ability to run sudo (Super User Do) administrative commands.

- We can now interact with our Ubuntu distribution through the bash console that was launched.

#### 1.2 Set up a WSL development environment

**Documentation & Instructions**: [https://docs.microsoft.com/en-us/windows/wsl/setup/environment#set-up-your-linux-username-and-password](https://docs.microsoft.com/en-us/windows/wsl/setup/environment)

- Upgrade your packages using the apt package manager by running ```sudo apt update && sudo apt upgrade``` in the launched bash console.

- You can open the new file system that comes with our Ubuntu distribution by leveraging the Windows explorer. To do this, enter the home directory and start the explorer executable from your Bash console as follows:
```cd ~```
```explorer.exe .```

### 2 Windows Terminal

Windows Terminal is a modern application that allows the use of many command-line shells like Command Prompt, PowerShell and bash (via Windows Subsystem for Linux) in a beautiful customizable terminal with features such as multiple tabs and panes, Unicode and UTF-8 character support and a GPU accelerated text rendering engine.

**Documentation**: [https://docs.microsoft.com/en-us/windows/terminal/](https://docs.microsoft.com/en-us/windows/terminal/)

#### 2.1 Installing Windows Terminal from the Microsoft Store
**Documentation & Instructions**: [https://docs.microsoft.com/en-us/windows/terminal/install](https://docs.microsoft.com/en-us/windows/terminal/install)

- Install Windows Terminal from the Microsoft Store by following this link: [https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=de-de&gl=DE](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=de-de&gl=DE).
- Once Windows Terminal is installed, search for Terminal in the Windows start menu and start the application. We can also pin Terminal to our Windows taskbar for easy accessibility in the future.

#### 2.2 Set up Windows Terminal

- Configure "Ubuntu" as your Startup Default profile as described in [https://docs.microsoft.com/en-us/windows/terminal/install#set-your-default-terminal-profile](https://docs.microsoft.com/en-us/windows/terminal/install#set-your-default-terminal-profile).
