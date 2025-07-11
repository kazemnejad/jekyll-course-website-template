---
layout: lab
title: "Lab 01: Software Setup"
date: 2025-07-07
---
# Goal

In today's Lab session, we will:

- Install Git, VS code, and Python (via Miniconda).
- Create a Github account and link it to VS code.
- Create a directory and a virtual environment for our course.
- Create a group website.

# I. Git and Github

## I.0. Verify Your Installation

- If you don't have a **Github** account, go to [I.1](#i1-create-a-github-account).
- Open **Terminal** (Mac) or **Command prompt (cmd)** (Windows).
- Type `git config list` and press enter.
  - If your name and email address of your **Github** account are correctly displayed, you already setup **Git** properly. Go to [II](#ii-vs-code).
  - If you get an error message `command not found`, follow steps in [I.2](#i2-installation) and [I.3](#i3-git-configuration).

## I.1. Create a Github Account

- Go to <https://github.com> and create a new account.
- Use your **primary** email address.

## I.2. Installation

**Mac**

- The installation will start automatically and may take some time. However, there's a faster method available <a href ="https://brew.sh/">(Homebrew)</a> . If the estimated time exceeds 10 minutes, please let us know.

**Windows**

- Go to <https://git-scm.com/downloads/win> and download the installer.
- During installation, when prompted for setting PATH environment, choose 'Git from the command line and also from 3rd-party software'.

### After installation

- Open **Terminal** (Mac) or **cmd** (Windows).
- Type `git --version` and press enter.
- If **Git** is successfully installed, then the version number will be displayed. Now, go to [I.3](#i3-git-configuration).

## I.3. Git Configuration

- Open **Terminal** (Mac) or **cmd** (Windows).
- Set your name: `git config --global user.name <name>`.
- Set your email: `git config --global user.email <email>`. Here, `<email>` should be your **github account email**.
- To check your configuration: `git config --list`. Press `q` to exit.

# II. VS Code

## II.0. Verify Your Installation

- Open **Terminal** (Mac) or **cmd** (Windows).
- Type `code .` and press enter.
  - If you get an error message `command not found`, follow steps in [II.1](#ii1-installation) and [II.2](#ii2-link-to-github).
- Click the profile icon at the bottom left.
  - If you can see your **Github** acount, then you already linked your Github account to VS code. Go to [II.3](#ii3-extensions).
  - If not, go to [II.2](#ii2-link-to-github).

## II.1. Installation

- Go to <https://code.visualstudio.com/Download> and download the installer.
- **(Mac)** After installation, move **Visual Studio Code.app** to the **Applications** folder.
- **(Windows)** During installation, check "Add to PATH".

### After installation

**Mac**

- Open **VS Code**.
- Press `Cmd+Shift+P`, type `Shell Command`, and click `install 'code' command ...`.
- Open **Terminal** and type `code .`, then press enter. If **VS Code** is open, you're done. Go to [II.2](#ii2-link-to-github).

**Windows**

- Open  **cmd** and type `code .`, then press enter. If **VS Code** is open, you're done. Go to [II.2](#ii2-link-to-github).

## II.2. Link to Github

- Open **VS code**.
- Click the profile icon at the bottom left.
- Click `Backup and Sync Settings`.
- Click `Sign in`, then choose `Sign in with Github` and follow instructions.
- *(Optional)* Activate **Github Copilot**.

## II.3 Extensions
- Click the extension icon on the left sidebar.
- Search and install `Python`, `Pylance`, `Jupyter` extensions.

# III.Python (Miniconda)
## III.0. Verify Your Installation
- Open **Terminal** (Mac) or **cmd** (Windows).
- Type `conda --version` and press enter.
  - If your version is not very outdated (latest: 25.5.1), you may use it. Go to [IV](#iv-virtual-environment).
  - If not, update by running `conda update conda`. After updating, check the version again, and go to [IV](#iv-virtual-environment).
  - If you get an error message `command not found`, follow steps in [III.1](#iii1-installation).

## III.1. Installation

- Go to <https://www.anaconda.com/download/success> and download the installer for **Miniconda**.
- **(Windows)** During installation, check "Add Miniconda3 to my **PATH** environment variable".

### After Installation

- Open **Terminal** (Mac) or **cmd** (Windows).
- You may see `(base)` on your terminal.
- Type `conda --version` and press enter.
- If **Miniconda** is successfully installed, then the version number will be displayed. Now, go to [IV](#iv-virtual-environment).

# IV. Virtual Environment
- Create a new directory anywhere on your computer (e.g. create `cosmos` in Desktop).
- Download <a href ="https://github.com/wonjun-seo/cosmos/blob/master/static_files/environment.yml">this file</a> and locate it to the folder you created.
- Open VS Code.
- Click File -> Open Folder... -> choose the folder you created.
- Click Terminal -> New Terminal
- Type `conda env create` and press enter. This creates conda environment `cosmos` with specified packages in `environment.yml` file in your computer.
- Type `conda activate cosmos`. This activates the environment `cosmos`. You may see `(cosmos)` on your terminal.
- Create `test.py` and select `cosmos` interpreter. Run `print("Hello, world")`.
- Create `test.ipynb` and select `cosmos` kernel. Run `print("Hello, world")`.
- Download <a href ="https://github.com/wonjun-seo/cosmos/blob/master/static_files/example.ipynb">this file</a> and locate it to the folder you created.
- Open the file on VS Code and run it.

# V. Create a Group Website
Every group will create a group website to present their final project.

- Go to <https://github.com/wonjun-seo/cosmos-demo> and follow the instructions. Only one member in each group should create a repository.


## Assignments

Update member information on the group website!

# Tomorrow

In tomorrow's lab session, we will work on basic Python coding and repository management using Git.
