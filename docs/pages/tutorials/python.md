---
title: Writing Your First Snake in Python
permalink: /tutorials/python
layout: card
---

This document will allow you to start developing a Battlesnake snake AI on a Windows 10/8/7 computer using the Python programming language.

## Step 1 - Download and Install Software

### Step 1.1 - Git

Git is a version command tool to allow us to "checkout" the NodeJS starter snake from Github.com.

Start by going to the [Git website](https://git-scm.com/downloads) and downloading the Windows version. Go to your Downloads folder, double-click on the the downloaded EXE file, and follow the installation steps. The installation will ask you a few questions during the process:

* You can configure which components get installed during the setup, but for now leave everything in this screen checked as-is.
* When asked what editor you want as your default to be used by Git, select your currently installed/favourite code editor from the dropdown or leave it as "vim".
* When asked about adjusting your PATH, don't change it and click next.
* Use the OpenSSL library when asked and click next.
* For configuring line ending conversions, choose "Checkout as-is, commit Unix-style line endings" and click next.
* Don't change the terminal emulator, click next.
* Don't change the extra options when asked, click install then click finish.

If you decide to perform all your commands from the command line then you will need to know about a new application called `Git Bash`. This is a minimal linux-style `bash` terminal console. Don't worry about the details of it, just know that we'll be using this to execute commands in the following steps.

---

### Step 1.2 - Git Extensions (optional)

There are many tools out there that make Git a little more user friendly. One of them is called Git Extensions. Go to the [Git Extensions](https://sourceforge.net/projects/gitextensions/) website and download and install. This tutorial does not get into the details of Git Extensions. It's really just a graphical front end, and behind the scenes it calls Git the same way you would on the command line.

---

### Step 1.3 - Python

Here you must decide whether you want to download [Python 2.7.x](https://www.python.org/downloads/release/python-2715/)

## Step 2 - Battlesnake Game Engine

The Engine is the piece of software that talks to your snake and asks it what moves to make next based on the current state of the game. It is available as a pre-packaged binary file complete with an interface to view and test your snake as you work on it.

### Step 2.1 - Download the Engine

* Go to <https://github.com/battlesnakeofficial/engine/releases/latest> and download the `Windows_x86_64.zip` file.
* Once downloaded, open Windows Explorer and navigate to your Downloads folder. Right-click and extract the downloaded ZIP file. It will extract into a folder of the same name.

---

### Step 2.2 - Run the Engine

Engine has a "dev" mode allows you to access a development environment that runs completely local to your machine. Running the engine in this way allows you to make quick iterations to your snake before putting it up on <https://play.battlesnake.com>.

* Open the folder with the game engine
* Shift + Right Click and select "Open command window here"
* At the prompt type:
    ```cmd
    engine.exe dev
    ```
* Minimize the console window then open your browser and go to the following URL: <http://localhost:3010>

What you should see is a web-based environment to test your snake locally before you put it on the Internet. Of course, we don't yet have a snake to test and that is what the next step will accomplish. Minimize this browser window as we'll use it later.

## Step 3 - Get a snake

### 3.1 - Download the Python starter snake

All the starter snakes are on github at <https://github.com/battlesnakeofficial/community/blob/master/starter-snakes.md>. You don't need a github account to download the Python starter snake, however this guide assumes you do have a github account (it's free).

* Go to <https://github.com/battlesnakeofficial/starter-snake-python>
* It is highly recommended to **Fork** the repository. This creates your own personal copy of the starter snake, so you can modify it and upload the changes. Go to the top right corner of the page and hit "Fork".
* Now you will want to **clone** the repository. Cloning places a copy of all the files from the repository onto your computer so you can modify them.
* You can get a link for cloning your repository by clicking "Clone or Download" and copying the link (we will use it below).

You can clone the starter snake using Git Bash or Git Extensions:

Git Bash:

* Open a new `Git Bash` console window. In the new console window, download the Python starter snake using git with the following command:
    ```bash
    git clone https://github.com/<your username>/starter-snake-python.git
    ```

Git Extensions:

* Start Menu >> Clone Repository
* In "Repository to Clone: Enter `https://github.com/<your username>/starter-snake-python.git`
* Choose a directory to install into and press "Clone"

---

### 3.2 - Install Python Dependencies

You can also find similar instructions from **README.md** in your new repository

* Go into your new starter snake folder
* Shift + Right Click and select "Open command window here"
* At the prompt type:
    ```cmd
    pip install -r requirements.txt
    ```

---

### 3.3 - Run the snake

Now you should be able to run the starter snake from a command line (or git bash):

```cmd
python app\main.py
```

If everything has gone well so far, open your browser again to <http://localhost:3010> and add your snake by pasting in the snake url of `http://localhost:8080` and clicking "Start Game" and then "Play". Your snake will probably die within a couple of turns because it's not very smart.

## Step 4 - Make your snake smart

### Step 4.1 - Coding

Now you can start modifying your snake's code and making it do something more exciting than hit a wall or running into itself.

---

### Step 4.2 - Push to Github

Assuming you forked the repository, you should be able to submit changes locally to your git repository and then push your changes back to github. There are lots of tutorials online on how to use Git (or Git Extensions).

## Step 5 - Deploy it to the Internet

Have a look at the `README.md` file in your starter-snake-node directory for instructions on deploying to Heroku.
