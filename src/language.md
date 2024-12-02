# Python language

This chapter discusses important things to note about the Python language beyond simple syntax. It covers libraries
and their management within the scientific Python ecosystem and code-editors.

Before embarking on a tutorial learning the Python language, it is recommended to follow this chapter and create an
'environment'. Within this new environment one should experiment, learning the language. Environments are described
below.

Once an environment has been created and selected, one can execute a Python program in the command-line using

```
(playground-environment) >>> python3 test_script.py
```

where `playground-environment` is the name of the Python environment. Alternatively, environments can be selected and
scripts launched using most code-editors such as VSCode.

Excellent educational resources for learning the Python language include:

- Free quick guide [www.freecodecamp.org](https://www.freecodecamp.org/news/the-python-guide-for-beginners/)
- Non-interactive guide [www.w3schools.com](https://www.w3schools.com/python/)
- Looks good, interactive [futurecoder.io](https://futurecoder.io/)
- Non-interactive guide [www.geeksforgeeks.org](https://www.geeksforgeeks.org/python-programming-language-tutorial/)

## Libraries and Packages

Users of other languages will be familiar with software libraries. These are algorithms which can be included and used
from one's own code. For example, a datetime library might help calculate the day given a date. It would be inefficient
to re-invent such functionality. Where possible, using a good library is a good idea.

In Python, libraries are called **packages**. In general libraries themselves use other libraries and packages are no
exception. A project that directly uses a few packages might indirectly need many more because those few may each need
other packages. Packages used by a project are described as that project's **dependencies**.

In even simple EM analyses, there can be *hundreds* of dependencies. Furthermore each package will require a specific
version of each dependency. Managing this manually is practically impossible. **Package managers** are programs that
install and organise this web if dependencies. 

Python has a built-in package manager called **pip**. This is not recommended for EM analysis projects. This is because
it stuggles to handle dependencies that include compiled code (such as C or Fortran maths libraries) or require access
to the GPU.

It is recommended to use the **Anaconda** package manager. This is free and one does not need to create an account.

## Anaconda Package Manager Variants

The Anaconda package manager comes in two variants. One includes a graphical user interface and many packages and
programs (such as code-editors) built-in (called **Anaconda Navigator**). The other is command-line only and comes with
a minimal set of packages built-in (often called **miniconda** or simply conda). In either case, they both facilitate
the installation of packages and their management. If you have done much programming before or are comfortable with the
command-line, use miniconda.

## Python Environments

It is very common to require a certain set of dependencies for one Python project and a different set for a different
project. It is inadvisable to solve this problem by installing a massive set of packages. This is because they are not
all mutually compatible and updating things will be a nightmare...

Instead it is strongly recommended to **use seperate environments**. A Python environment contains the Python
interpreter (the program that reads and executes Python code) and a set of packages. These environments are isolated
from one another. This has numerous advantages

- Breaking one environment doesn't break others
- Breaking one environment won't break Anaconda's environment and thereby prevent fixing
- Mutually incompatible packages can be used (in seperate environments)
- Updating is much much faster because each environment is smaller
- It is easy to know exactly the dependencies of a project, greatly simplifying reproducibility
- Running someone else's code is much easier because their environment can be recreated exactly

Before running code one must select the environment. This can be done in the command-line, within many code-editors
(see below) or within Anaconda Navigator.

The default environment with Anaconda is `base`. This contains all the dependencies used by Anaconda. **Do not install
anythin into the base environment.** Instead, create a new environment and install things there.

To create a new environment and install dependencies with Anaconda Navigator, use
[this](https://docs.anaconda.com/navigator/tutorials/manage-environments/) guide. To create and manage environments
with miniconda, use [this](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
guide.

A list of suggested packages for a first EM analysis environment can be found in [Ecosystem Chapter](ecosystem.md).

## Editing code

Python code is text, it can be edited with any text editor such as Notepad or GNU Nano. Don't do that.

An integrated development environment (**IDE**) contains a text editor and other tools (such as easy selection of
Python environment). There is a spectrum of complexity, from the simplest text editors (such as Notepad) to the most
complex IDEs (such as JetBrain's *PyCharm*).

While choice of IDE is a personal preference, **VSCode** (and formerly **Spyder**) are the most popular in the
scientific community. Therefore one should use VSCode if unsure.

With VSCode, the Python tools are installed as *extensions*. When opening any *.py* Python file, installation of these
is prompted. Install the recommended plugins.

When editing a Python file in VSCode, the currently selected environment is shown in the lower right. It will show
something like `Python  3.11.6 ('env_name': conda)` where 'env_name' is the name of the currently selected environment.
To select a different environment, click the environment name. A popup will be displayed at the top of the window where
a different environment can be selected.
