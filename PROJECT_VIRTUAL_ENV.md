## Create and Manage your Project Virtual Environment

To keep our project separate from all other Python projects, we will create and manage a local project virtual environment.
We'll install our packages into the local project virtual environment.  
The steps in this common workflow are listed below.
Details and commands used are provided in the following sections.

1. Open your project folder in VS Code.
2. Open a terminal window in VS Code (PowerShell for Windows, zsh or bash for Mac/Linux). 
3. Use git pull first, to make sure you have the current project on your machine.
4. Use venv to create a new .venv environment in the repo on your machine. 
5. Activate your environment using the command for your operating system. 
6. Use pip to install necessary packages into your active project virtual environment.
7. Edit your README.md to record your commands, process, and notes.
8. Git add / commit / push to GitHub.
9. Verify your work.

### 1.1. Open Project in VS Code

Open the project folder on your machine (the one you cloned from GitHub into your Documents folder) if not already open. 

### 1.2. Open VS Code Terminal

Open a terminal window in VS Code (PowerShell for Windows, zsh or bash for Mac/Linux). 

### 1.3. Git Pull

In the terminal, run git pull to fetch any changes that might have been made to the GitHub version.
There may not be any changes, but it's good practice to pull every time you start work on a git project. 

```shell
git pull
```

### 1.4. Create Project Virtual Environment

Use your terminal to create your project virtual environment by running venv as a Python module (py -m venv) and providing a name to use for the local folder as .venv.
If you name it differently, be sure that your folder name is included in the .gitignore file. 

Windows command

```shell
py -m venv .venv
```

Mac/Linux command

```
python3 -m venv .venv
```

You should get a new folder in your project repository named .venv. 
If VS Code asks to use use this environment, click Yes. 

### 1.5. Activate the Project Virtual Environment

Use your terminal to activate your project virtual environment. (Do this every time you open a new terminal to work on your project.)

Windows commands to activate your .venv. Try the first. Use the second if the first doesn't work. 

```shell
.venv\Scripts\Activate
.\.venv\Scripts\Activate.ps1
```

Mac/Linux command to activate your .venv

```shell
source .venv/bin/activate
```

Verify you see the virtual environment name (.venv) in your terminal prompt.

### 1.6. Install Packages into Active Environment

Verify your project virtual environment located in .venv is active.
If not, activate it. 
You should see .venv in your terminal prompt. 
Use your favorite method to install the necessary packages.

At this point, the only project dependencies we know we need are:

- pika - allows us to use RabbitMQ with Python
 
Windows command to install project dependencies:

```shell
py -m pip install pika
```

Mac/Linux command to install project dependencies:

```shell
python3 -m pip install pika
```

OR: Use requirements.txt to install packages instead

If you like, you can use a [requirements.txt](requirements.txt) file to install dependencies instead.
These files are helpful in projects when we have several external packages to install and it can be good practice.

To do so, you'll need a file named requirements.txt in the root folder of your repository listing each external package used, one per line. 

If using Windows PowerShell, install into your active project virtual environment with this command:

```shell
py -m pip install -r requirements.txt
```

If using Mac or Linux, install into your active project virtual environment with this command:

```shell
python3 -m pip install -r requirements.txt
```

If successful, you will now be able to use the following line in your Python scripts.
If you get an error on this line, work through the steps above to
create, activate, and install into your local project virtual environment,
and make sure VS Code is using your .venv local project environment. 

```
import pika
```

### 1.7. Edit README.md

Edit your README.md file to record your commands, process, and notes.
Use one hash followed by a space for the title.
Use two hashes followed by a space to create second level headings. 
Use triple back tics on a line by themselves to "fence" your code.
 

### 1.8. Git Add / Commit / Push to GitHub

Use your terminal to add your files to source control, commit your changes to git, and push them up to GitHub. 

Git add any new files.

```shell
git add .
```

Git commit changes.

```shell
git commit -m "after .venv setup"
```

Git push to GitHub. 

```shell
git push -u origin main
```

### 1.9. Verify

Verify your README.md and .gitignore (and optionally, requirements.txt if used) appear correctly in your GitHub repo.
Since you added .venv/ to your .gitignore, your .venv folder should NOT appear in GitHub.
This is good - it saves space and allows us to track just the progress of our project files. 
