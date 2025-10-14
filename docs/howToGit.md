# How To Git
The general workflow is to start a stage in the directory(s) that you want to affect, then start commiting changes. Generally `Commit and Push` is fine unless multiple people have edited the GitHub repository you're pulling from in which case you might want their changes with `Commit and Sync`.

All of this can be done from the **Source Control** tab in VSC.

## Setting Everything Up
### Software
The easiest part will be installing everything. You'll need to grab the following software:

1. A code editor. I'm using [*Visual Studio Code (VSC)*](https://code.visualstudio.com/Download) since it's what I'm familiar with and it has great plugin support. It also has a pretty sleek and friendly UI for source control.
2. [*Git*](https://git-scm.com/downloads). You can leave everything on default settings if you're installing it for the first time. No Git knowledge is required since we'll be doing our source control inside of *VSC*.
3. [*Python*](https://www.python.org/downloads/) - I'm using version 3.13 but you can use 3.14 if you wish.

> On VSC, you'll also need the follow extensions and any prerequisites they install:
>
> 1. Python
> 2. Python Environments

### Creating the workspace
A workspace is VSC's version of a file explorer. The root will be whatever folder you tell VSC to open up initially - we'll be using a virtual environment to make sure whatever we write isn't depenendent on any modules we unknowingly installed. This section can be confusing so I recommend not rushing through it. Doing so will likely result in a messy workspace which matters since:

1. You'll want to use the `mkdocs serve` for testing an offline version of the site. The only other way to preview your changes would be to push your commits to the testing branch which is prohibited.
2. We care about making the contribution process easy for ourselves. While you could just edit a .gitignore file to reduce the organizational issues stemming from a messy workspace, this keep things visually tidy.

#### Setting up the virtual environment
1. In the *Tool Bar* at the top, go to **File > Open folder**.
2. Create a folder somewhere that will hold all your files. You can call it *LESSDocumentWorkspace*.
3. Open that folder using *VSC*. You should see a new, empty explorer UI on the left side now.
4. Using `Ctrl + Shift + P` will open up the *VSC* command terminal. Look for `Python: Create Virtual Environment`.
5. Executing the command will create a new .venv folder with all the files you need to run a virtual environment inside.

The .venv is now created but you'll need to activate a script in order to actually use it. We'll come back to it after we clone the repository.

At this point you can technically contribute to the repository

#### Cloning the repository
Before you can clone the repository for editing, you'll need a few things: