# streaming-03-rabbitmq

> Get started with RabbitMQ, a message broker, that enables multiple processes to communicate reliably through an intermediary.

This project requires some free code - beyond that available in the Python Standard Library. To avoid messing up our local default Python installation, and any other Python projects we may have, we  create a local virtual environment to install and use these libraries.

Think of a virtual environment as a safe sandbox. 
We can install whatever we want in our sandbox, and it won't break other Python projects that may require different versions, etc. 

We use the built-in Python utility `venv` to create our virtual environment. 
There are other options, but this is simplest and most common. 
We create the environment as a subfolder of this repo named .venv to keep it away from our project code. 

## Prerequisites

1. Git
1. Python 3.11+ preferred
1. VS Code Editor
1. VS Code Extension: Python (by Microsoft)
1. RabbitMQ Server installed and running locally

See the Markdown page for your operating system to verify RabbitMQ is installed and running on your machine before attempting to continue. 

- [Linux](RABBIT_INSTALL_VERIFICATION_LINUX.md)
- [macOS](RABBIT_INSTALL_VERIFICATION_MACOS.md)
- [Windows](RABBIT_INSTALL_VERIFICATION_WINDOWS.md)

:chart: Display a screenshot here that verifies your RabbitMQ is installed and running.

## Before You Begin - Start A New Project

Follow this common workflow to start a new project by using this starter repo. 

1. In your browser, fork this repository into your own GitHub account. 
2. Clone your new GitHub repository down to your machine into your Documents folder.
3. Open your project folder in VS Code (if you haven't already).
4. In VS Code, if it doesn't already exist, add a useful .gitignore with a line for .vsode/ and .venv/ and whatever else doesn't need to go in the repo. Here's an example [.gitignore](.gitignore).
6. In VS Code, edit your README.md to record your commands, process, and notes so far.
7. Open a terminal in VS Code - PowerShell if Windows, zsh or bash if Mac/Linux.
8. Git add and commit with a useful message (e.g. "initial commit") and push to GitHub.

## Task 1. Create and Manage your Project Virtual Environment

We will use pika, which is not included in the Python Standard Library. We must install it. 
To keep our project separate from all other Python projects, we will create and manage a local project virtual environment.
We'll install our packages into the local project virtual environment.
For the recommended process with detailed steps and commands, see [PROJECT_VIRTUAL_ENV.md](PROJECT_VIRTUAL_ENV.md).

## Optional - Utility Scripts 

In your VS Code terminal window, you may try to run the following commands to help verify your setup.
These util files MAY be helpful to ensure you're setup correctly. 
You may have a different configuration and RabbitMQ may still work; the check looks in common places, but may not work for all installations. 
They are meant to be helpful, but are not required.

You can help by updating the code for other common configurations. 
Just fork the current repo, add your change, and create a pull request (no other changes please) and I'll pull it back in. 
If Mac/Linux, use python3 instead of py. Or python. Whatever works on your machine. 

```shell
py util_about.py
py util_aboutenv.py
py util_aboutrabbit.py
py -m pip list
```

![verifying setup](./images/verifying.png)


## Task 2. Read

1. Read the [RabbitMQ Hello World! tutorial](https://www.rabbitmq.com/tutorials/tutorial-one-python.html)
1. Read the code and comments in our 2 project files: emit_message.py and listen_for_messages.py

Don't worry if it doesn't all make sense the first time. 
Approach it like a puzzle and see what you can figure out. 

## Task 3. Execute the Producer/Sender

Read v1_emit_message.py (and the tutorial)

Run the file on Windows:

```shell
py v1_emit_message.py
```

Run the file on Mac/Linux:

```shell
python3 v1_emit_message.py
```

It should run, emit a message to the named RabbitMQ queue, and finish.
We can execute additional commands in the terminal as soon as it finishes. 

## Task 4. Execute the Consumer/Listener

Read v1_listen_for_messages.py (and the tutorial)

Run the file on Windows:

```shell
py v1_listen_for_messages.py
```

Run the file on Mac/Linux:

```shell
python3 v1_listen_for_messages.py
```

You'll need to fix an error in the program to get it to run.
Once it runs successfully, will it terminate on its own? How do you know? 
As long as the process is running, we cannot use this terminal for other commands. 

## Task 5. Open a New Terminal / Emit More Messages

1. Open a new terminal window.
1. Use this new window to run emit_message.py again.
1. Watch the listing terminal - what do you see?  A second message?

:chart: Display a screenshot here that shows your two terminal windows communicating successfully. 

Sending the same message each time is kind of boring. This time:

1. Where is the message defined? How can you change it?
1. Modify emit_message.py to emit a different message. 
1. Execute the updated emit_message.py. 
1. Watch what happens in the listening terminal.

Repeat this process several times - emit at least 4 different messages.
Don't worry - it's just code. We can always revert back (try the 'undo' command in VS Code) to a version that works. You can't hurt anything.

## Task 6. Save Time & Effort: Don't Repeat Yourself

Did you notice you had to change the message in TWO places?

1. You update the actual message sent. 
1. You also update what is displayed to the user. 
1. Fix this by introducing a variable to hold the message. 
1. Use your variable when sending. 
1. Use the variable again when displaying to the user. 

Now, to send a new message, you'll only make ONE change.
Updating and improving code is called 'refactoring'. 
Use your skills to keep coding enjoyable. 

## Version 2

Now look at the second version of each file.
These include more graceful error handling,
and a consistent, reusable approach to building code.

Each of the version 2 programs include an error as well. 

1. Find the error and fix it. 
1. Compare the structure of the version 2 files. 
1. Modify the docstrings on all your files.
1. Include your name and the date.
1. Imports always go at the top, just after the file docstring.
1. Imports should be one per line - why?
1. Then, define your functions.
1. Functions are reusable logic blocks.
1. Everything the function needs comes in through the arguments.
1. A function may - or may not - return a value. 
1. When we open a connection, we should close the connection. 
1. Which of the 4 files will always close() the connection?
1. Search GitHub for if __name__ == "__main__":
1. How many hits did you get? 
1. Learn and understand this common Python idiom.

## Reference

- [RabbitMQ Tutorial - Hello, World!](https://www.rabbitmq.com/tutorials/tutorial-one-python.html)
- [Using Python environments in VS Code](https://code.visualstudio.com/docs/python/environments)
- [RabbitMQ Get Started](https://www.rabbitmq.com/#getstarted)
- [What is RabbitMQ? IBM Intro Video 10 min](https://www.youtube.com/watch?v=7rkeORD4jSw)

![Exploring the local virtual environment folder](./images/exploring_dot_venv.PNG)
