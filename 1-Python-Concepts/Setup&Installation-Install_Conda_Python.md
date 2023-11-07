# Python Installation- Cont'd


### 4 Miniconda & Python

Miniconda is a small bootstrap version of Anaconda that includes only conda, Python and the packages they depend on as well as a small number of other useful packages including pip, zlib and few others. Anaconda is the world’s most popular open-source Python distribution platform and one of its main components, conda, is an open-source package and environment management system that runs on Windows, macOS, and Linux. With conda, we can quickly install, run, and update packages and their dependencies. It allows us to easily create, save, load, and switch between environments on our local computer, thus enabling isolated, project-specific environment management. Conda was initially created for Python programs, but it can package and distribute software for any language. 

**Documentation**: [https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html)

#### 4.1 Install Miniconda with Python 3.10 in WSL

**Window and Linux**

In case you have conda installed

- In the bash command line interface Terminal (WSL Ubuntu profile), go back to the root directory by
  
```cd ..```

- In case you have conda installed already, check the updates by
  
- Run the following to download the Miniconda installation script

```wget https://repo.anaconda.com/miniconda/Miniconda3-py310_23.1.0-1-Linux-x86_64.sh```

- Then, run this command to install Miniconda
```bash Miniconda3-py310_23.1.0-1-Linux-x86_64.sh``` and follow the prompts on the installer screens. Answer "yes" to all questions, particularly to whether you wish the installer to initialize Miniconda3 by running conda init.

- Afterwards, you can remove the installation command

  ```rm Miniconda3-py310_23.1.0-1-Linux-x86_64.sh```
 

- To make the installation changes take effect, close and then re-open your terminal window.

- Run the command
 ```conda list``` 
 
 This command is used to verify that conda is now installed. If an output of packages is returned, you are good to go.
 - In case it tells you that the conda command was not found. Run ```bash``` and then run ```conda list``` again.

**Alternative**
Download the appropriate installer for your OS with the latest Python version(Python 3.10) from [here](https://docs.conda.io/en/latest/miniconda.html)

#### 4.2 Create the Conda Environment

We will now create our first conda environment to install all required packages and libraries for the lessons. The most reproducible and recommended way to install a conda environment is from an environment definition in a ".yml" file. To this end, the repository that we just cloned in the previous step contains an "environment.yml" file where the Python version as well as all required packages including their respective versions are defined. We can install the conda environment from the "environment.yml" file as follows:

- Run 

```cd ReDI-Intro-to-Python```

```conda env create -f environment.yml```

This installs the conda environment defined in the "environment.yml" file. **Note**: When using WSL, Conda may fail to connect to the Anaconda repo and return a CondaHTTPError. If that is the case, open the Windows Command Prompt and type ```wsl --shutdown```. This will restart WSL. Then open WSL and try again.

- After the installation is done, run 

```conda env list``` 

This will list all conda environments. Next to the "base" environment, which is installed by default, you should now see the environment named "intro-to-python".

- We can activate the new environment by running 

```conda activate intro-to-python```

 We will activate this environment at the beginning of every lesson of Python classes. In your day-to-day work, we recommend creating different conda environments for different projects so that you have isolated environments and don't break things because of incompatibility of packages across projects.

- To deactivate the new environment, run 

```conda deactivate```.

- OPTIONAL: to uninstall the newly installed conda environment, run 

```conda env remove -n intro-to-python```.

<!-- ### 1.2.5 Azure CLI 

The Azure Command-Line Interface (CLI) is a cross-platform command-line tool to connect to Azure and execute administrative commands on Azure resources. It allows the execution of commands through a terminal using interactive command-line prompts or a script.

**Documentation**: [https://docs.microsoft.com/en-us/cli/azure/what-is-azure-cli](https://docs.microsoft.com/en-us/cli/azure/what-is-azure-cli)

#### 1.2.5.1 Install Azure CLI

**Documentation & Instructions**: [https://docs.microsoft.com/de-de/cli/azure/install-azure-cli](https://docs.microsoft.com/de-de/cli/azure/install-azure-cli)

- Run ```curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash``` to install the Azure CLI.

#### 1.2.5.2 Install Azure CLI Azure ML Extension

- Run ```az extension add -n azure-cli-ml``` to install the Azure CLI Azure ML Extension.

### 1.2.6 Terraform

Terraform is an open-source infrastructure as code software tool that enables you to safely and predictably create, change, and improve infrastructure.

**Documentation**: [https://www.terraform.io/](https://www.terraform.io/)

#### 1.2.6.1 Install Terraform

**Documentation & Instructions**: [https://learn.hashicorp.com/tutorials/terraform/install-cli](https://learn.hashicorp.com/tutorials/terraform/install-cli)

- Run ```sudo apt-get update && sudo apt-get install -y gnupg software-properties-common``` to ensure that your system is up to date, and you have the gnupg, software-properties-common, and curl packages installed. You will use these packages to verify HashiCorp's GPG signature, and install HashiCorp's Debian package repository.
- Run ```wget -O- https://apt.releases.hashicorp.com/gpg | gpg --dearmor | sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg``` to install the HashiCorp GPG key.
- Run ```gpg --no-default-keyring --keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg --fingerprint``` to verify the key's fingerprint.
- Run ```echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list``` to add the official HashiCorp repository to your system.
- Run ```sudo apt update``` to download the package information from HashiCorp.
- Run ```sudo apt-get install terraform``` to install Terraform from the new repository.

### 1.2.7 Docker

Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime.

**Documentation**: [https://docs.docker.com/](https://docs.docker.com/)

#### 1.2.7.1 Install Docker

**Documentation & Instructions**: [https://medium.com/geekculture/run-docker-in-windows-10-11-wsl-without-docker-desktop-a2a7eb90556d](https://medium.com/geekculture/run-docker-in-windows-10-11-wsl-without-docker-desktop-a2a7eb90556d)

- Run ```sudo apt update``` to updated the local repository.
- Run ```sudo apt install docker.io -y``` to install Docker.
- Run ```docker --version``` to check the Docker installation.
- Enable automatic start of Docker Daemon on WSL:
    - Modify /etc/sudousers file, which controls how sudo command are executed. We need to make the following modifications to start dockerd without being prompted for a password every time you start a terminal window. Run ```sudo visudo``` and add the following to the bottom of the file: 
        - ```
          # Docker daemon specification
          <USERNAME> ALL=(ALL) NOPASSWD: /usr/bin/dockerd
          ``` 
          (Please replace `<USERNAME>` with your username).
    - Open the .bashrc file by running ```nano ~/.bashrc```. Then add the following to the bottom of the file:
         -  ```
            # Start Docker daemon automatically when logging in if not running.
            RUNNING=`ps aux | grep dockerd | grep -v grep`
            if [ -z "$RUNNING" ]; then
                sudo dockerd > /dev/null 2>&1 &
                disown
            fi
            ```
    - Add your username to docker group so you can run docker as a non-root user by running ```sudo usermod -aG docker <USERNAME>```. Again, replace `<USERNAME>` with your username.
- Validate the Docker installation by running ```docker run hello-world```.

--- -->
