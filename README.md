## IDE (Integrated Development Environment):

__1) Pycharm:__
- PyCharm is an integrated development environment (IDE) specifically designed for Python development.
- You can download PyCharm from (https://www.jetbrains.com/pycharm/download/?section=windows). There are two versions available i.e. Professional version and Community version (free).
- After successfully installing PyCharm, you need to add new environment variables. Setting environment variables for PyCharm can be done at the system level or by using PyCharm run configuration.
- To set environment variables at the system level on Windows, go to (Edit the system environment variables -> Environment variables -> under User variables, select Path -> Click Edit -> Click New -> Add [C:\Users\omkar\AppData\Local\Programs\Python\Python312\ & C:\Users\omkar\AppData\Local\Programs\Python\Python312\Scripts] -> Click Ok -> Click Ok -> Click Ok.

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/f2b570b0-fd4b-4590-9341-b337d97c223c)

__2) VS code:__
- VS Code is a free integrated development environment (IDE) developed by Microsoft.
- It supports multiple languages and comes with features such as debugging, syntax highlighting, intelligent code completion, snippets, code refactoring, and embedded Git, which is very convenient for version control.
- It offers numerous settings and a vast marketplace with extensions for adding new languages, themes, debuggers, and connecting additional services.
- Working with VS Code can enhance your efficiency as a data scientist. It can manage your entire data science project lifecycle.
- You can download VS Code from (https://code.visualstudio.com/download)
- To open VS Code in specific folder, right click -> Open in terminal -> run code command.

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/2f255810-d9f8-4485-b5fa-b4bf38c70e4c)

__3) Anaconda:__
- To use Jupyter Notebook, you need to download Anaconda, which is available for download (https://www.anaconda.com/download).
- Jupyter Notebook is not a traditional integrated development environment (IDE). It is an open-source web application that enables you to create and share documents containing live code, equations, visualizations, and narrative text.
- After successfully installing Anaconda, you need to add new environment variables. Setting environment variables for Jupyter can be done at the system level.
- To set environment variables at the system level on Windows, go to (Edit the system environment variables -> Environment variables -> under User variables, select Path -> Click Edit -> Click New -> Add [C:\Users\omkar\anaconda3\ & C:\Users\omkar\anaconda3\Scripts] -> Click Ok -> Click Ok -> Click Ok.
- To open Jupyter in specific folder, right click -> Open in terminal -> run jupyter notebook command.

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/3fb73c31-00e7-432a-9ecd-a7745ba61e4e)

## Conda environment:
- Conda environments provide a way to isolate different projects, preventing conflicts between dependencies and package versions required by different projects.
- Creating a Conda environment is crucial for maintaining a clean, organized, and reproducible development environment. It helps manage dependencies, reduces conflicts, and enhances overall efficiency and reliability in Python projects.
- Environments allow you to manage specific versions of Python and other packages for a particular project. By specifying exact dependency versions, Conda environments make it easier to share code, enabling others to recreate the same environment without issues.
- Conda simplifies package management with a single tool for installing, updating, and removing packages, making it more user-friendly than manual dependency management.
- With Conda, you can easily switch between different Python versions for different projects, particularly beneficial for projects with specific Python version requirements.

__Conda commands:__
| Command                                                                      | Use                                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| conda info                                                                   | Used to verify whether conda is installed or not                                                                 |
| conda --version                                                              | Used to check conda version                                                                                      |
| conda update conda                                                           | Used to update conda to the latest version                                                                       |
| conda env list                                                               | Used to get a list of all my environments (active environment is shown with *)                                   |
| conda list                                                                   | List all packages and versions installed in an active environment                                                |
| conda create --name your_env_name                                            | Create a new environment                                                                                         |
| conda create --name your_env_name python=3.x                                 | Create a new environment with a specific python version                                                          |
| conda create --name your_env_name python=3.x package1 package2 ...           | Create a new environment with specific packages                                                                  |
| conda env create --file environment.yml                                      | Create a new environment from a YAML file (in yml file env_name is already present)                              |
| conda create --name your_env_name --file requirements.txt                    | Create a new environment from a TXT file (in txt file env_name is not present so that you need to give env_name) |
| conda create --name your_env_name python=3.x && conda activate your_env_name | Create a new environment and activate it                                                                         |
| conda activate your_env_name                                                 | Activate specified environment                                                                                   |
| conda deactivate your_env_name                                               | Deactivate specified environment and switch back to base environment                                             |
| conda env remove --name your_env_name                                        | Delete specified environment                                                                                     |
| conda create --clone source_env_name --name new_env_name                     | To make exact copy of a specified conda environment                                                              |
| conda install package_name                                                   | Install a specific package to a currently active environment                                                     |
| conda install --name your_env_name package_name                              | Install packages in a specific environment                                                                       |
| conda update package_name                                                    | Update a package in the current environment                                                                      |
| conda install package_name=1.2.3                                             | Install a specific version of a package to a currently active environment                                        |
| conda install package1 package2 package3                                     | Install multiple packages at once to a currently active environment                                              |
| conda install -c channel_name package_name                                   | Install packages from a specific channel to a currently active environment                                       |
| conda install -c channel_name package_name=1.2.3                             | Install packages from a specific channel and version to a currently active environment                           |
| conda install --file requirements.txt                                        | Install packages using a .TXT file to currently active environment                                               |
| conda install --name your_existing_env_name --file requirements.txt          | Install packages using a .TXT file to a specified environment                                                    |
| conda env update --name your_existing_env_name --file environment.yml        | Install packages using a .YML file to a currently active environment                                               |
| conda list --export > requirements.txt                                       | To Generate .TXT file from a currently active environment                                                               |
| conda env export --name your_env_name > requirements.txt                     | To Generate .TXT from specified conda environment                                                                |
| conda list --export > environment.yml                                        | To Generate .YML from a currently active environment                                                                    |
| conda env export --name your_env_name > environment.yml                      | To Generate .YML from a specified conda environment                                                              |

__Ways to specify version numbers:__
| Specification         | Result                              |
|-----------------------|-------------------------------------|
| numpy=1.11            | 1.11.0, 1.11.1, 1.11.2, 1.11.18 etc |
| numpy==1.11           | 1.11.0                              |
| "numpy>=1.11"         | 1.11.0 or higher                    |
| "numpy=1.11.1|1.11.3" | 1.11.1, 1.11.3                      |
| "numpy>=1.8,          | 1.8, 1.9, not 2.0                   |

__Difference between yml and txt file:__

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/7ac97e53-ee7f-403d-bcfc-8902d0b8d799)

![image](https://github.com/omkarfadtare965/Essential/assets/154773580/2b7eb970-556d-4f3c-ae8f-15294df568c8)
