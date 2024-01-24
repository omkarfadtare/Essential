# Essential steps to set-up your System:
## Setting up an IDE (Integrated Development Environment):
### 1) Pycharm:
- PyCharm is an integrated development environment (IDE) specifically designed for Python development.
- You can download PyCharm [here](https://www.jetbrains.com/pycharm/download/?section=windows). There are two versions available i.e. Professional version and Community version (free).
- After successfully installing PyCharm, you need to add new environment variables. Setting environment variables for PyCharm can be done at system level or by using PyCharm run configuration.
- To set environment variables at the system level on Windows:
  - Go to, edit the system environment variables
  - Environment variables
  - Under user variables select Path
  - Click Edit
  - Click New
  - Add (C:\Users\omkar\AppData\Local\Programs\Python\Python312\ & C:\Users\omkar\AppData\Local\Programs\Python\Python312\Scripts)
  - Click Ok
  - Click Ok
  - Click Ok
- You can find path and version of Python using below commands

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/f2b570b0-fd4b-4590-9341-b337d97c223c)

### 2) VS code:
- VS Code is a free and open source integrated development environment (IDE) developed by Microsoft.
- It supports multiple languages and comes with features such as debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and embedded Git, which is very convenient for version control.
- It offers numerous settings and a vast marketplace with extensions for adding new languages, themes, debuggers, and connecting additional services.
- Working with VS Code can enhance your efficiency as a Data scientist. It can manage your entire data science project lifecycle.
- You can download VS Code [here](https://code.visualstudio.com/download).
- To open VS Code in specific folder:
  - Right click
  - Open in terminal
  - Run `code` command

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/2f255810-d9f8-4485-b5fa-b4bf38c70e4c)

### 3) Anaconda:
- To use Jupyter notebook, you need to download Anaconda. You can download Anaconda [here](https://www.anaconda.com/download).
- Jupyter notebook is not a traditional integrated development environment (IDE). It is an open-source web application that enables you to create and share documents containing live code, equations, visualizations, and narrative text.
- After successfully installing Anaconda, you need to add new environment variables. Setting environment variables for Jupyter can be done at the system level.
- To set environment variables at the system level on Windows:
  - Go to, edit the system environment variables
  - Environment variables
  - Under sser variables select Path
  - Click Edit
  - Click New
  - Add (C:\Users\omkar\anaconda3\ & C:\Users\omkar\anaconda3\Scripts)
  - Click Ok
  - Click Ok
  - Click Ok
- To open Jupyter in specific folder:
  - Right click
  - Open in terminal
  - Run `jupyter notebook` command
- You can find path and version of Jupyter notebook using below commands

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/3fb73c31-00e7-432a-9ecd-a7745ba61e4e)

## Conda environment:
- Conda environment provides a way to isolate different projects, preventing conflicts between dependencies and package versions required by different projects.
- Creating a Conda environment is crucial for maintaining a clean, organized, and reproducible development environment. It helps manage dependencies, reduces conflicts, and enhances overall efficiency and reliability in Python projects.
- Environments allow you to manage specific versions of Python and other packages for a particular project. By specifying exact dependency versions, Conda environments make it easier to share code, enabling others to recreate the same environment without issues.
- Conda simplifies package management with a single tool for installing, updating, and removing packages, making it more user-friendly than manual dependency management.
- With Conda, you can easily switch between different Python versions for different projects, particularly beneficial for projects with specific Python version requirements.
- Use Conda prompt or Command promt or VS Code powershell (ctrl + `) for Conda operations.

__Conda commands:__
| Command                                                                      | Use                                                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| conda info                                                                   | Used to verify whether Conda is installed or not                                                                   |
| conda --version                                                              | Used to check Conda version                                                                                        |
| conda update conda                                                           | Used to update Conda to the latest version                                                                         |
| conda env list                                                               | Used to get a list of all environments (active environment is shown with *)                                        |
| conda list                                                                   | List all packages and versions installed in an active environment                                                  |
| conda create --name your_env_name                                            | Create a new environment                                                                                           |
| conda create --name your_env_name python=3.x                                 | Create a new environment with a specific python version                                                            |
| conda create --name your_env_name python=3.x package1 package2 ...           | Create a new environment with a specific python version and specific packages                                      |
| conda env create --file environment.yml                                      | Create a new environment from a .YAML file (in .YML file env_name is already present)                              |
| conda create --name your_env_name --file requirements.txt                    | Create a new environment from a .TXT file (in .TXT file env_name is not present so that you need to give env_name) |
| conda create --name your_env_name python=3.x && conda activate your_env_name | Create a new environment with a specific python version and activate it                                            |
| conda activate your_env_name                                                 | Activate specific environment                                                                                      |
| conda deactivate your_env_name                                               | Deactivate specific environment and switch back to base environment                                                |
| conda env remove --name your_env_name                                        | Delete specific environment                                                                                        |
| conda create --clone source_env_name --name new_env_name                     | To make exact copy of a specific environment                                                                       |
| conda install package_name                                                   | Install a specific package to a currently active environment                                                       |
| conda install --name your_env_name package_name                              | Install packages in a specific environment                                                                         |
| conda update package_name                                                    | Update a package in a currently active environment                                                                 |
| conda install package_name=1.2.3                                             | Install a specific version of a package to a currently active environment                                          |
| conda install package1 package2 package3                                     | Install multiple packages at once to a currently active environment                                                |
| conda install -c channel_name package_name                                   | Install packages from a specific channel to a currently active environment                                         |
| conda install -c channel_name package_name=1.2.3                             | Install packages from a specific channel with a specific python version to a currently active environment          |
| conda install --file requirements.txt                                        | Install packages using a .TXT file to a currently active environment                                               |
| pip install -r requirements.txt                                              | Install packages using a .TXT file to a currently active environment (preferred way)                               |
| conda install --name your_existing_env_name --file requirements.txt          | Install packages using a .TXT file to a specific environment                                                       |
| conda env update --name your_existing_env_name --file environment.yml        | Install packages using a .YML file to a currently active environment                                               |
| conda list --export > environment.yml                                        | To generate .YML file from a currently active environment (error due to formatting)                                |
| conda env export --name your_env_name > environment.yml                      | To generate .YML file from a specific environment (error due to formatting)                                        |
| conda list --export > requirements.txt                                       | To generate .TXT file from a currently active environment (error due to formatting)                                |
| conda env export --name your_env_name > requirements.txt                     | To generate .TXT file from a specific environment (error due to formatting)                                        |
| conda list -e > requirements.txt                                             | To generate .TXT file from a currently active environment (error due to formatting)                                |
| pip freeze > requirements.txt                                                | To generate .TXT file from a currently active environment (error due to formatting)                                |
| pip list --format = freeze > requirements.txt                                | To generate .TXT file from a currently active environment (works fine this is the preferred way)                   |

__Ways to specify version numbers:__
| Specification         | Result                              |
|-----------------------|-------------------------------------|
| numpy=1.11            | 1.11.0, 1.11.1, 1.11.2, 1.11.18 etc |
| numpy==1.11           | 1.11.0                              |
| "numpy>=1.11"         | 1.11.0 or higher                    |
| "numpy=1.11.1|1.11.3" | 1.11.1, 1.11.3                      |
| "numpy>=1.8,          | 1.8, 1.9, not 2.0                   |

__Difference between .YML and .TXT file:__

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/7ac97e53-ee7f-403d-bcfc-8902d0b8d799)

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/2b7eb970-556d-4f3c-ae8f-15294df568c8)

## Version control systems & Repository hosting services:
__Terminology:__
- Remote repository is a repository on GitHub account, whereas Local repository is repository in your local machine/computer.

### Version control systems:
__1) Git:__
- Git is a distributed version control system or tool that enables collaboration among multiple contributors by allowing them to work on the same project concurrently.
- It helps you manage and track changes in your code or project over time.
- Git can be used through the command line interface, but various GUI tools, such as GitKraken or GitHub Desktop, provide a visual interface for those who prefer not to use the command line interface, but as a programmer it's always a good practice to use terminal.

__2) GitKraken:__
- GitKraken is a graphical user interface (GUI) for Git, providing a visual representation of your repositories. Visualizes branches, commits, and merges.

__3) GitHub Dekstop:__
- GitHub Dekstop is another graphical user interface (GUI) for Git, providing visual representations and simplifying common Git operations.

__4) SVN (Subversion):__
- SVN is a centralised version control system that helps software developers manage and track changes in their code over time.
- It allows multiple people to work on the same project simultaneously, keeping a history of modifications, and facilitating collaboration.

### Repository hosting services: 
- GitHub, GitLab, and Bitbucket are online platforms where you can store, collaborate, and manage your code that uses Git as the version control system. While they share the fundamental purpose of hosting repositories, they may differ in additional features, integrations, and the overall development ecosystem they offer.

__1) GitHub:__
- GitHub is a web-based platform, owned by Microsoft, for hosting and collaborating on Git repositories. It's like a cloud-based space to store and work on your code.
- It provides Git repository hosting, code collaboration, issue tracking, and integration with various development tools.
  
__2) GitLab:__
- GitLab is also a web-based platform for hosting Git repositories, similar to GitHub.
- It offers a complete DevOps platform, encompassing not only version control but also continuous integration and deployment (CICD).
- It provides Git repository hosting, continuous integration, deployment tools, code review, issue tracking, and more—all within a single platform.

__3) Bitbucket:__
- Bitbucket is also a web-based platform for hosting Git repositories, owned by Atlassian, similar to GitHub and GitLab.
- It provides Git repository hosting, code collaboration, integration with other Atlassian products (such as Jira), and support for both Git and Mercurial repositories.

### Authentication methods in git:
- When connecting your local machine to a GitHub account or remote repository using Git, you need an authentication method. Here are several commonly used methods:

__1) HTTPS:__
- HTTPS authentication in Git uses username and password for authentication but GitHub deprecated password authentication for Git operations in August 2021.
- So it is recommended to use a Personal Access Token (PAT) instead of your account password.
- Easy to set up, but may require entering credentials again and again.

> Steps to generate PAT:
  - Go to GitHub settings
  - Developers settings
  - Personal access token
  - Token (classic)
  - Generate new token
  - Generate new token (classic)
  - Enter your GitHub password
  - Confirm
  - Set expiry date for token
  - Select scope of token
  - Generate token.
  - Use generated personal access token as a password during Git operations

__2) GCM (Git Credential Managers):__
- Enhances authentication by caching credentials.
- GCM is a one-time process, often requires logging in with a browser.
- By default, GCM is installed at the time of Git installation.
- If GCM is not installed in system you can download GCM from [here](https://github.com/git-ecosystem/git-credential-manager/releases) 

> Step to check whether GCM is installed or not using below command in Git Bash:
  - ```ruby
    git credential-manager-core --version
    ```
    
__3) SSH (Secure Shell) Keys:__
- SSH keys provides a more secure method for authentication.
- It requires generating an SSH key pair and adding the public key to your GitHub account.
- It enables secure communication via the SSH protocol.

> Steps to generate and set SSH key:
  - Open Git Bash and write below command:
  - ```ruby
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
    ```
  - Specify location and name of the file to be saved
  - You can optionally set a passphrase for added security. Press Enter to skip or enter a passphrase when prompted.
  - SSH key will be generated and saved to the specified location
  - View SSH public key using below command:
  - ```ruby
    cat file_path.pub
    ```
  - Copy SSH public key
  - Add SSH private key to SSH Agent using below command:
  - ```ruby
    eval "$(ssh-agent -s)"
    ssh-add E:/file_path
    ```
  - Add copied SSH public key to GitHub or Git hosting services, go to GitHub account
  - Settings
  - SSH and GPG keys
  - New SSH key
  - Give a title (just for your reference)
  - Paste SSH public key
  - Add SSH key
  - Enter Github password
  - Confirm

## Git branching simplified:
- Branching is extremely useful because when building new features for an application that might break your code or are not yet finished, you don't want to save them directly to the main master branch. Instead, you want to work on them in a kind of sandbox, a separate branch. This way, you can write and refine the code until it's correct and in the state you want, before merging it back into the main code base. This approach is especially helpful when multiple people are working on the same repository or when there are numerous branches in progress simultaneously.
- Git branching is like creating separate paths to work on different tasks without messing up the main project.
- It's like having different notebooks for different tasks, such as writing a story or drawing. This way, you can make changes and try out new ideas without affecting the main story until you're sure you want to include them. Once you're happy with your work in a branch, you can bring those changes back into the main project.
- Developers use branches to isolate changes, experiment with new features, or fix bugs without affecting the main codebase until they are ready to be merged.
- It allows developers to isolate changes, experiment with new features, or fix bugs without affecting the main codebase until they are ready to be merged.
- It helps in managing complexity by allowing developers to work on different tasks independently.
- It reduces conflicts by isolating changes in separate branches until they are ready to be integrated.
- It facilitates a more controlled and efficient development process, especially in collaborative environments.

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/38bf13f5-9148-4202-808a-1b6b9fe4d433)

> Types of Branch in Git:

__1) Master/Main Branch:__
- The master (or main) branch is typically the default branch in a Git repository. It represents the stable, production-ready version of the code. Your main workspace where all the finished code lives.

__2) Feature Branch:__
- Developers create special areas to work on new things called "feature branches." Feature branches are like special areas for working on new features without disturbing the main project.
- Changes made in a feature branch can be brought back into the main project when ready. It's a way to keep everything neat and tidy while trying out and adding exciting features.
- When we create a new feature branch, initially, the code on the master branch and this new feature branch will be exactly the same. As you make updates and commit those changes to the feature branch, those updates are only visible in the feature branch. Similarly, when you make updates and commit changes to the master branch, those changes are only seen in the master branch.
- Each branch keeps track of the changes made on that specific branch. The changes made in one branch are isolated to that branch until they are explicitly merged into another branch.

__3) Bugfix Branch:__
- These are used to fix specific bugs without affecting the main code. Similar to feature branches, bugfix branches are created off the master branch.

__4) Release Branch:__
- These branches are created before releasing a new version for final testing. They are merged into both master and development branches once ready.

__5) Development/Branch-per-feature workflow:__
- In some workflows, each feature or task is developed in its own branch. Once the feature is complete, it is merged back into the main branch.
























Python programming
- Introduction
- OOPS (Object oriented programming)
- Numpy
- PAndas
- Regex
- Data types in Python
- Sci-Kit learn
- MatPlotLib
- Seaborn
- NLTK
- Tensorflow
- Keras
- Automl
- Optical character recognition (OCR)
- Hello world

Learning Path
- Python
- Machine learning
- Deep learning
- Natural language processing
- AWS
