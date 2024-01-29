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
- You can find path and version of Python by running below commands in command prompt:

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
- You can find path and version of Jupyter notebook by running below commands in command prompt:

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/3fb73c31-00e7-432a-9ecd-a7745ba61e4e)

## Conda environment:
- Conda environment provides a way to isolate different projects, preventing conflicts between dependencies and package versions required by different projects.
- Creating a Conda environment is crucial for maintaining a clean, organized, and reproducible development environment. It helps manage dependencies, reduces conflicts, and enhances overall efficiency and reliability in Python projects.
- Environments allow you to manage specific versions of Python and other packages for a particular project. By specifying exact dependency versions, Conda environments make it easier to share code, enabling others to recreate the same environment without issues.
- Conda simplifies package management with a single tool for installing, updating, and removing packages, making it more user-friendly than manual dependency management.
- With Conda, you can easily switch between different Python versions for different projects, particularly beneficial for projects with specific Python version requirements.
- Use Conda prompt or Command promt or VS Code powershell (ctrl + `) for Conda operations.

### Conda commands:
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

## Git and GitHub:
__Terminology:__
- Remote repository is a repository on GitHub account, whereas Local repository is repository in your local machine/computer.

### Version control systems:
__1) Git:__
- Git is a distributed version control system or tool that enables collaboration among multiple contributors by allowing them to work on the same project concurrently.
- It helps you manage and track changes in your code or project over time.
- Git can be used through the command line interface or VS Code terminal or Git Bash, but various GUI tools, such as GitKraken or GitHub Desktop, provide a visual interface for those who prefer not to use the command line interface, but as a programmer it's always a good practice to use terminal.
> Installing Git Bash:
- You can download and install Git Bash [here](https://git-scm.com/downloads).

__2) GitKraken | Tower:__
- GitKraken is a graphical user interface (GUI) for Git, providing a visual representation of your repositories. Visualizes branches, commits, and merges.
- Tower is a popular Git client that provides a graphical user interface (GUI) for managing Git repositories. It is not an intrinsic part of Git itself but is a third-party tool that facilitates Git-related tasks.

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
> Creating a GitHub account:
- You can create and set-up your GitHub account [here](https://github.com/).
  
__2) GitLab:__
- GitLab is also a web-based platform for hosting Git repositories, similar to GitHub.
- It offers a complete DevOps platform, encompassing not only version control but also continuous integration and deployment (CICD).
- It provides Git repository hosting, continuous integration, deployment tools, code review, issue tracking, and more—all within a single platform.

__3) Bitbucket:__
- Bitbucket is also a web-based platform for hosting Git repositories, owned by Atlassian, similar to GitHub and GitLab.
- It provides Git repository hosting, code collaboration, integration with other Atlassian products (such as Jira), and support for both Git and Mercurial repositories.

### Authentication methods in Git:
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
```ruby
git credential-manager-core --version
```
    
__3) SSH (Secure Shell) Keys:__
- SSH keys provides a more secure method for authentication.
- It requires generating an SSH key pair and adding the public key to your GitHub account.
- It enables secure communication via the SSH protocol.
> Steps to generate and set SSH key:
  - Open Git Bash and write below command:
```ruby
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
  - Specify location and name of the file to be saved
  - You can optionally set a passphrase for added security. Press Enter to skip or enter a passphrase when prompted.
  - SSH key will be generated and saved to the specified location
  - View SSH public key using below command:
```ruby
cat file_path.pub
```
  - Copy SSH public key
  - Add SSH private key to SSH Agent using below command:
```ruby
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

### Git branching simplified:
- Branching is extremely useful because when building new features for an application that might break your code or are not yet finished, you don't want to save them directly to the "main/master" branch. Instead, you want to work on them in a kind of sandbox, a separate branch. This way, you can write and refine the code until it's correct and in the state you want, before merging it back into the main code base. This approach is especially helpful when multiple people are working on the same repository or when there are numerous branches in progress simultaneously.
- Git branching is like creating separate paths to work on different tasks without messing up the main project.
- It's like having different notebooks for different tasks, such as writing a story or drawing. This way, you can make changes and try out new ideas without affecting the main story until you're sure you want to include them. Once you're happy with your work in a branch, you can bring those changes back into the main project.
- Developers use branches to isolate changes, experiment with new features, or fix bugs without affecting the main codebase until they are ready to be merged.
- It allows developers to isolate changes, experiment with new features, or fix bugs without affecting the main codebase until they are ready to be merged.
- It helps in managing complexity by allowing developers to work on different tasks independently.
- It reduces conflicts by isolating changes in separate branches until they are ready to be integrated.
- It facilitates a more controlled and efficient development process, especially in collaborative environments.
> Steps to prepare files to Push them from local to remote repository:

__1) git add:__ This command is used to stage changes for the next commit.

__2) git commit:__ This command creates a new commit with the changes that have been staged (added) using "git add".

__3) git push:__ This command is used to upload local repository commits to a remote repository.

> Types of branch:
- Every Git repository typically contains at least one long-running branch, commonly named "main/master". Additional long-running branches, such as "developement" or "production" or "integration" may exist throughout the entire project lifecycle. These branches often represent different stages in the release or deployment process. It is common to structure branches to mirror the flow of code through various states, such as development, staging, and production.
- Changes are not directly merged to these branches; instead changes are merged to the "integration" branch, this ensures only tested and reviewed code is introduced into production environments.
- This practice aligns with the principles of testing, code review, and release bundling, allowing for controlled and scheduled releases. In contrast to long-running branches, short-lived branches are created for specific purposes and are deleted after integration. Common use cases for short-lived branches include working on new features or bug fixes. These branches provide isolation for changes, allowing developers to collaborate on specific tasks without impacting the main development branches.

__1) Long lived branch:__
- Long lived branches are branches that exist throughout the entire lifespan of a project. For example "main/master" branch, "developement" branch, "production" branch, "integration" branch.
- Changes are carefully merged into these branches after thorough testing and review, ensuring that only well-vetted code becomes a permanent part of the project's history.

__2) Short lived branch:__
- Short lived branches are branches that are created for a specific, temporary purpose and are not intended to exist throughout the entire lifespan of the project. For example "feature_branch", "bug_fix_branch", "release_preparation_branch", "experiment_branch".

__3) Master/Main branch:__
- The "master/main" branch is typically the default branch in a Git repository. It represents the stable, production-ready version of the code. Your main workspace where all the finished code lives.

__4) Feature branch:__
- Developers create special areas to work on new things called "feature_branch". These branches are like special areas for working on new features without disturbing the main project.
- Changes made in a "feature" branch can be brought back into the main project when ready. It's a way to keep everything neat and tidy while trying out and adding exciting features.
- When we create a new "feature_branch", initially, the code on the "master" branch and this new "feature_branch" will be exactly the same. As you make updates and commit those changes to the "feature_branch", those updates are only visible in the "feature_branch". Similarly, when you make updates and commit changes to the "master" branch, those changes are only seen in the "master" branch.
- Each branch keeps track of the changes made on that specific branch. The changes made in one branch are isolated to that branch until they are explicitly merged into another branch.

__5) Bugfix branch:__
- These are used to fix specific bugs without affecting the main code. Similar to "feature_branch", "bug_fix_branch" are created off the master branch.

__6) Developement branch:__
- The "development" branch serves as a central place where developers integrate their changes and collaborate on new features or improvements before these changes are merged into more stable branches, such as a "production" or "main/master" branch.

__6) Integration/Staging branch:__
- "Integration/Staging" branch generally refers to a branch where different changes from various developement branches are brought together, integrated, and tested as a whole before being merged into a more stable branch or released into production.

__7) Production branch:__
- "Production" branch refers to a long-lived branch that represents the stable and reliable version of the software that is deployed to the production environment.

__8) Release branch:__
- These branches are created before releasing a new version for final testing. They are merged into both "master/main" and "development" branches once ready.

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/38bf13f5-9148-4202-808a-1b6b9fe4d433)

### Branching strategies:
1) Gitflow
2) GitHub flow  

__1) Gitflow:__
- It is a branching model that defines specific roles for different branches.
- Main branch -> Developement branch -> Feature branch -> Release branch -> Hotfix branch 

__2) GitHub flow:__
- It is a simplified and continuous delivery-oriented branching model.
- Main branch -> Feature branch

### Git Bash simplified:

__1) Pushing local repository to GitHub account:__
- Open local project folder having project files in it and copy folder path
- Open Git Bash and set username and email address
```ruby
git config --global user."user_name"
git config --global email."email_address"
```
- Check for present working directory in Git Bash
```ruby
pwd
```
- Change present working directory of Git Bash to the project folder path (copied folder path)
```ruby
cd /e/copied_folder_path
```
- Go to GitHub account and create a new repository (local and remote repository name can be differnet, doesn't have to be same) without initializing README file
- Come back to Git Bash and run below command
```ruby
git remote add origin https://github.com/user_name/remote_repo_name.git
git status
```
- Stage, commit and push all the files to the remote repository
```ruby
git add .
git commit -m "Commit message"
git push
```

__2) Pushing changes madde in local repository to remote repository:__
- After making changes run below commands:
```ruby
git add .
git commit -m "commit_message"
git push
```

__3) Clonning remote repository from GitHub account to local machine:__
- Goto GitHub account and initialize a new repository with README file and copy the HTTPS web url
- Open Git Bash, navigate to the desired path and run below command:
```ruby
cd /e/
git clone copied_web_url
```

__4) Pulling changes made in remote repository to local repository:__
- Open Git Bash, navigate to the local repository on your machine and run any of the below two commands in Git Bash:
```ruby
git fetch origin
git merge
```
```ruby
git pull
```
- "git fetch" will check are there any new changes in remote repository which are not available in your local repository. It's more like counting how many changes are avialable.
- Whereas "git pull" will fetch and merge/update local repository with all the aviable changes in remote repository.

![image](https://github.com/omkarfadtare/Essential/assets/154773580/03ba2592-fa02-4d29-bc91-5849a9b3eeb9)

__5) Creating a new branch:__
- Open Git Bash, navigate to the project folder and run below commands:
```ruby
pwd
cd /e/Project
git branch
git checkout -b bug_fix_branch
git branch
git checkout main
git checkout bug_fix_branch
```
- When we create a new "bug_fix" branch, initially, the code on the "main/master" branch and this new "bug_fix_branch" will be exactly the same. As you make updates and commit those changes to the "bug_fix_branch", those updates are only visible in the "bug_fix_branch". Similarly, when you make updates and commit changes to the "main/master" branch, those changes are only seen in the "main/master" branch.

__6) Merging branch or branch changes:__
- Merging in Git is the process of integrating changes from one branch, for example a "feature_branch" into another branch, for example "main/master" branch. 
- Run either of the below commands in Git Bash to review the differences between branches before merging:
```ruby
git diff
git diff main..feature_branch
git diff feature_branch..main
git log -p feature_branch
```
- Commit changes on your branch, push them to the remote repository.
```ruby
git add .
git commit -m "commit message"
git push
```
- Create a pull request to propose merging your changes into the target branch from GitHub.
- Once the pull request is approved and merged, you typically delete the "feature_branch" and switch back to the "main/master" branch.
- You can directly merge changes from "feature_branch" to "main/master" branch by running below Git command to bypass the process of review that pull requests facilitate:
```ruby
git merge feature_branch
```
- You can directly merge changes from "main/master" branch to "feature_branch" by running below Git command to bypass the process of review that pull requests facilitate:
```ruby
git merge main
```
- However, for collaborative projects or when changes need to be reviewed by others before being merged into the "main/master" branch, creating a pull request is the preferred workflow. 
- Pull requests allow for code review, discussion, and collaboration among team members, ensuring that changes are thoroughly vetted before being merged into the "main/master" branch.
- In such cases, the merging typically occurs on the hosting platform (like GitHub) after the pull request has been approved.

__7) Pull requests:__
- Pull requests are a way for team members to discuss and review code changes before they are merged into the "main/master" branch. They're like asking for a second opinion on your work.
- For instance, when you finish working on a feature, instead of directly merging your code into the "main/master" branch, you create a pull request. This allows other team members to review your changes, provide feedback, and suggest improvements.
- Once everyone agrees that the code looks good, the pull request can be approved and the changes are merged into the "main/master" branch. It's a collaborative way to ensure code quality and prevent mistakes from being introduced into the project.

![image](https://github.com/omkarfadtare/Essential/assets/154773580/d0e430eb-3332-4c93-be1b-2250b804b35a)

__8) Deleting branch:__
- If you've merged the changes from "bug_fix_branch" into another branch or "main/master" branch, and then deleted "bug_fix_branch" from the remote repository on GitHub, your local repository might still be tracking the branch. This can happen because Git keeps a local reference to the remote branches, untill you explicitly remove them locally.
- To update your local repository and remove the reference to the deleted branch run below commands in Git Bash:
```ruby
git fetch --prune
git branch -d bug_fix_branch
git branch
```
- If you haven't merged "bug_fix_branch" yet and still want to delete the branch you may need to force delete it by running below command in Git Bash:
```ruby
git branch -D bug_fix_branch
```

__9) Undoing changes in Git:__
- If you accidentally added files to the staging area (that is "git add"), you can undo this to unstage the files, by running below command in Git Bash:
```ruby
git reset
git reset file_name
```
- If you make a mistake in a commit message or accidentally commit changes, you can undo the commits by running below command in Git Bash:
```ruby
git reset HEAD~1.
```
- Here, "HEAD~1" refers to the previous commit. You can specify the number of commits to go back if needed.
- To find the commit you want to reset to, run below command in Git Bash to view the commit history and find the commit hash (the unique identifier for each commit):
```ruby
git log
```
- Once you have the commit hash, run below command in Git Bash to reset to that specific commit. Be cautious as this will discard any changes made after that commit:
```ruby
git reset --hard commit_hash
``` 

__10) Merge conflicts:__
- Merge conflicts occur when Git is unable to automatically merge changes from different branches. This happens when multiple people modify the same part of a file, or when changes made in one branch conflict with changes made in another branch.
- Merge conflicts arise when Git cannot determine which changes to keep because of overlapping same modifications in different branches.
- There are couple of ways to resolve merge conflicts but the best way is to use Merge editor in VS Code:
- Open the conflicted file(s) in a code editor(VS Code)
- Locate the conflict markers (<<<<<<<, =======, >>>>>>>) and manually resolve the conflicting changes.
- Save the files after resolving the conflicts.
- Stage the resolved files using "git add" and then commit the changes using "git commit -m "commit message"".

![image](https://github.com/omkarfadtare/Essential/assets/154773580/fd421449-1fcc-4d4e-9d4a-9ebfdc6edb42)

- If you encounter difficulties resolving conflicts, you can abort the merge by running below command in Git Bash to return to the pre-merge state:
```ruby
git merge --abort
```
- Merging locally wasn't the regular pattern because the "main/master" branch gets updated with changes from other contributors while you're working on your own branch.
- It's crucial to stay up-to-date with these changes to avoid falling too far behind, making future merges more challenging. Therefore, it's recommended to regularly pull ("git pull") changes from the main branch into your local branch before merging ("git merge"). This ensures smoother integration of your work with the latest updates from the main branch.

__11) Forking repository:__
- Forking a repository on GitHub means copying someone else's project to your own GitHub account. It allows you to experiment and contribute to projects without altering the original code. It enables you to contribute to open-source projects by making changes and suggesting improvements.
- You can make changes, test new features, and fix bugs and if you want your changes to be part of the original project, you can create pull requests.
- To fork a repository on GitHub, simply navigate to the repository you want to fork and click the "Fork" button in the top-right corner of the page.
- Once forked, the repository will be copied to your GitHub account. You can access it from your account's repositories list.
- After forking, you can make changes to the code, create branches, and experiment with the project as needed.
- If you want your changes to be included in the original project, you can create pull requests from your forked repository to the original repository. The owner of the original repository can then review and merge your changes if they find them valuable.

### Git commands:


__Useful resources:__
- [Git for Beginners](https://www.youtube.com/watch?v=RGOj5yH7evk&list=PLLJ1hZKyeCH1I8dP0UNTpWoIhsl6KpVbu&index=2)
- [Git for Professionals](https://www.youtube.com/watch?v=Uszj_k0DGsg&list=PLLJ1hZKyeCH1I8dP0UNTpWoIhsl6KpVbu&index=3)
- [Git for Advanced users](https://www.youtube.com/watch?v=qsTthZi23VE&list=PLLJ1hZKyeCH1I8dP0UNTpWoIhsl6KpVbu&index=5)
