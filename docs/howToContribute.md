# How To Contribute

The general workflow is to start a stage in the directory(s) that you want to affect, then start commiting changes. Generally `Commit and Push` is fine unless multiple people have edited the GitHub repository you're pulling from in which case you might want their changes with `Commit and Sync`.

All of this can be done from the **Source Control** tab in VSC.

---
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

A workspace is VSC's version of a file explorer. In here, we'll keep all the relevant files we need to for writing technical documentation in VSC. The root will be whatever folder you tell VSC to open up initially. In the root, we'll have a folder for a virtual environment; it's to make sure whatever we write isn't depenendent on any modules we unknowingly installed. In another folder, we'll also have our local version of the repository. The local repository is how we'll be remotely working on any changes that will eventually be pushed to the repository hosted on GitHub. This section can be confusing so I recommend not rushing through it. Doing so will likely result in a messy workspace which matters since:

1. You'll want to use the `mkdocs serve` for testing an offline version of the site. Note that because we are using a virtual environment, you'll have to run the command every time you want to preview the change.
2. We care about making the contribution process easy for ourselves. While you could just edit a .gitignore file to reduce the organizational issues stemming from a messy workspace, this keep things visually tidy.

### Setting up the virtual environment

1. In the **Tool Bar** at the top, go to **File > Open folder**.
2. Create a folder somewhere that will hold all your files. This folder will be our workspace. You can call it *MyDocumentWorkspace* if you wish.
3. Open that folder using VSC. You should see a new, empty explorer UI on the left side now.
4. Using `Ctrl + Shift + P` will open up the **VSC command terminal**. Look for `Python: Create Virtual Environment`.
5. Executing the command will create a new *.venv* folder with all the files you need to run a virtual environment inside.

The virtual environment is now created. It'll automatically activate on initial creation; to access it, you'll need to open a new command prompt terminal. You can verify it's working if you see `(YourVenv'sName)` at the start of your command line prompt in the terminal. Any time you close Visual Studio Code or exit out of the virtual environment, you'll want to activate it again by opening the **VSC command terminal**, running `Python: Select Interpreter` and then selecting the *Python.exe* inside of your `.venv` folder.

To set up the virtual environment with the scripts we'll be using for contributing, you'll only need to run one command inside the virtual environment: `pip install mkdocs-material`. This will install all necessary files inside of the 

At this point you can technically contribute to the repository but passing off the changes through a file transfer. However, the point of learning all of this is to make it *easy* for you to contribute. Therefore, we now need to set up Git.

### Cloning the repository through Git and VSC

There are a few ways to go about cloning the repository, but I'll teach you the most straightforward way.

1. In VSC, make sure you're in the workspace established earlier (*MyDocumentWorkspace* if you've been following along).
2. In the **VSC command terminal**, select `Git: Clone`. For the URL, enter `https://github.com/KevinNokham/randominipedia`.
3. You now need to select a folder to store your local version of the repository. Whatever folder you select will contain all the cloned repository files starting at the repository's root level.
> Note that the location of this folder can be anywhere on your computer or even another remote storage device. For the purposes of this tutorial, I'll be creating a new folder called *myLocalRepository* in *MyDocumentWorkspace* and selecting that as the destination.

You now have a local, cloned repository of `randominipedia`. Any changes you make to the files here will be local only until you push it to one of the branches.