Virtual Environment Setup

- [1. What Is A Virtual Environment](#1-what-is-a-virtual-environment)
- [2. Requirements](#2-requirements)
- [3. Make Sure Pip is Installed and Up-To-Date](#3-make-sure-pip-is-installed-and-up-to-date)
- [4. Make Sure 'venv' Is Installed](#4-make-sure-venv-is-installed)
- [3. Determine the Location of Your Target Directory](#3-determine-the-location-of-your-target-directory)
- [4. Create Your Virtual Environment](#4-create-your-virtual-environment)
- [100. Freezing Your Virtual Environment](#100-freezing-your-virtual-environment)

# 1. What Is A Virtual Environment

A virtual environment allows you to create an isolated 'habitat' for your Python project to live. Each virtual environment has it's own Python binary, and can have its own independent set of installed Python packages in its site directories.

A virtual environment give you the freedom to experiment with different packages, libraries, & frameworks (etc.) without fear of making any changes to your computer's global state. When you're done with your virtual environment, you can delete it without any lasting repercussions.

Along with experimentation, proper use of virtual environments ensures that when you switch projects, you can simply create a new virtual environment without any concern of affecting the packages installed in other virtual environments.

As someone who originally learned Python through trial and error, rather than any formal education on the subject, knowledge of virtual environments and how to create & use them would have saved me a lot of time and headache early in my career.

The venv module provides support for creating lightweight “virtual environments” with their own site directories, optionally isolated from system site directories.

# 2. Requirements

Python 3.9

# 3. Make Sure Pip is Installed and Up-To-Date

[pip](https://packaging.python.org/key_projects/#pip) is the reference Python package manager, used to install & update packages. If you installed Python 3, pip is included, however it is easy enough to check with the following command:

```bash
python3 -m pip --version
```

You should use the newest version of pip when creating your virtual environment. The Python Documentation recommends to use the system pip to bootstrap a user installation / upgrade of pip, however if you are using a PATH other than the standard '/User/username/Library/Python3', you will want to remove the user flag:

With --user flag:

```bash
python3 -m pip install --user --upgrade pip
```

Without --user flag:

```bash
python3 -m pip install --upgrade pip
```

# 4. Make Sure 'venv' Is Installed

After ensuring that your version of pip is up-to-date, we want to install / check on the package that we will be using to create our virtual environment. The Python documentation states that if you are using Python 3.3 or newer, the [venv](https://docs.python.org/3/library/venv.html#module-venv) module is the preferred way to create and manage virtual environments. The venv package is included in the Python standard library & therefor requires no additional documentation.

Since we will be using Python 3.9 for this guide, we will be using the 'venv' package.

# 3. Determine the Location of Your Target Directory

Your 'target directory' is the folder that your virtual environment will exist on your computer. I would advise making a new folder (directory) for your virtual environment rather than using any existing directory in order to maintain the "isolated" integrity of your virtual environment.

I use a generalized 'Development' folder for any programming projects I'm working on, but the nature of a virtual environment makes it so that this isn't necessary (although I would still recommend it, especially if you're just starting out).

The Python documentation recommends to use a virtual environment while developing any Python applications.

In order to check your current directory using the terminal, you can use the following command, which will "Print Working Directory" for you:

```bash
pwd
```

# 4. Create Your Virtual Environment

Create a virtual environment by executing venv. If you are currently switched into the target directory you will be using for your working directory, you can use the 'env' argument to create your virtual environment.

The second argument of 'env' is the location of your virtual environment, so if you are not switched into your target directory, you can specify its location rather than using 'env'. If this is the case, replace the 'env' argument with the path to your target directory to create your virtual environment:

If you are switched into your target directory:

```bash
python3 -m venv env
```

if you are **not** switched into your target directory:

```bash
python3 -m venv /path/to/new/virtual/environment
```

# 100. Freezing Your Virtual Environment

Add information about freezing your virtual environment in order to pass the requirements to GitHub

Sources:
[Python Documentation - Installing Packages Using Pip & Virtual Environments](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment)
[Python Documentation - Creation of Virtual Environments](https://docs.python.org/3/library/venv.html)
