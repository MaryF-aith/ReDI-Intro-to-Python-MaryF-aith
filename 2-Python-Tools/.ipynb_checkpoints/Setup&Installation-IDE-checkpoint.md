# Python Installation- Cont'd


### 5 Visual Studio Code (VSCode)

Visual Studio Code, commonly referred to as VSCode, is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux. It comes with support for many languages including Python and has a rich ecosystem of useful extensions, e.g. for working with Git and Azure including a source control tab that will show your changes and handle a variety of git commands for you.. With VSCode we can take advantage of features like Intellisense code completion, linting, debug support, code snippets, and unit testing. Learn more about VS Code's Git support here:
https://code.visualstudio.com/docs/editor/versioncontrol#_git-support

**Documentation**: [https://code.visualstudio.com/docs](https://code.visualstudio.com/docs)

#### 5.1 Install VSCode

**Documentation & Instructions**: [https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode](https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode)

- Download  VS code installer file from [VS Code install page](https://code.visualstudio.com/download) for your OS. Then install Visual Studio Code on Windows (not in your WSL file system).


- When prompted to Select Additional Tasks during installation, be sure to check the Add to PATH option so you can easily open a folder in WSL using the code command.

<!-- #### 1.5.2 Install VSCode Remote Development Extension

- Install the [Remote Development extension pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack). This extension pack includes the Remote - WSL extension, in addition to the Remote - SSH, and Remote - Containers extensions, enabling you to open any folder in a container, on a remote machine, or in WSL. -->

#### 5.2 Open a WSL project in Visual Studio Code

- Open your Linux distribution's command line via Windows Terminal or just oopen your terminal in other OS and run

 ```code .```
 
  **Note:** it might take some time to install the VS Code Server if you run the command for the first time.

<!-- - You can also access more VS Code Remote options by using the shortcut: CTRL+SHIFT+P in VS Code to bring up the command palette. If you then type Remote-WSL you will see a list of the VS Code Remote options available, allowing you to reopen the folder in a remote session, specify which distribution you want to open in, and more. -->
<!-- 
#### 1.5.3 Install Python -->

<!-- - The Remote-WSL extension splits VS Code into a “client-server” architecture, with the client (the user interface) running on your Windows machine and the server (your code, Git, plugins, etc) running remotely in WSL.
- When running VS Code Remote, extensions can therefore be installed either on your local machine or in your WSL distribution (remote). Selecting the 'Extensions' tab will display a list of extensions split between your local machine and your WSL distribution. Extensions for the client (the user interface), like themes, are installed once on your local machine. Installing server extensions on the remote, like the Python extension, or anything that handles things like linting or debugging, must be done separately in your WSL distribution (once in each one if you have multiple). VS Code will display a warning icon ⚠, along with a green "Install in WSL" button, if you have an extension locally installed that is not installed in your WSL. -->
<!-- - Click on extension tab, you can also do that with the keyboard shortcut(Ctrl+Shift+X)
- NSearch for python and install python

ow install the [Python extension](https://marketplace.visualstudio.com/items?itemName=ms-python.python) in your WSL distribution. -->

### 6 JupyterLab

JupyterLab is the latest open-source web-based interactive development environment for notebooks, code, and data. As such, it is one of the most popular tools for Data Scientists. Its flexible interface allows users to configure and arrange workflows in data science, scientific computing, computational journalism, and machine learning. A modular design invites extensions to expand and enrich functionality.

**Documentation**: [https://jupyterlab.readthedocs.io/en/stable/](https://jupyterlab.readthedocs.io/en/stable/)

#### 6.1 Run JupyterLab 

- Activate the conda environment by opening your Linux distribution's command line via Windows Terminal or other terminals by running

```conda activate intro-to-python```

- Run 

```jupyter lab --no-browser``` 

This will launch JupyterLab. Copy the URL, open the browser of your choice on your local workstation (e.g. Google Chrome), and paste the URL into the address bar. (**Note**: don't close the terminal as we have started an interactive JupyterLab session, which will be terminated once you close your terminal. You can stop the interactive session by pressing "CTRL + C".)
- You can now work with notebooks (".ipynb" format) in JupyterLab and follow the hands-on python sessions. All packages that you will need during the Python classes are defined in the "environment.yml" file and have therefore been installed in your conda environment called "intor-to-cs". Since we started the JupyterLab session from within this environment, you have now access to all required packages.

## 7. Summary Remarks

Congratulations on making it until here! You have learned a great deal about different useful data science tools that can be leveraged to efficiently run analyses with your data and you have installed these tools on your local workstation so that you can use them for this class and your future projects. In addition, you have taken your first steps to learn Python, one of the most powerful general-purpose programming languages and the leading programming language among data scientists. Thanks to our conda environment, you will have all required Python packages to your availability and the only thing you have to worry about is activating the environment and running JupyterLab from within the environment.
