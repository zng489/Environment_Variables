# Environment_Variables

```
=================================================================================================================
python -m venv myenv
python -m venv myenv python=3.6
=================================================================================================================
conda create -n myenv
conda create -n myenv python=3.6
=================================================================================================================
```

# Gerenciando dependências do Python com pipenv
```
where python
C:\Users\Yuan>where python
C:\Users\Yuan\AppData\Local\Programs\Python\Python310\python.exe
C:\Users\Yuan\AppData\Local\Microsoft\WindowsApps\python.exe

pip install pipenv
C:\Users\Yuan>pip install pipenv


pip list
C:\Users\Yuan>pip list
Package                           Version
--------------------------------- ---------
backports.entry-points-selectable 1.1.0
certifi                           2021.10.8
distlib                           0.3.3
filelock                          3.3.1
pip                               21.2.3
pipenv                            2021.5.29
platformdirs                      2.4.0
setuptools                        57.4.0
six                               1.16.0
virtualenv                        20.8.1
virtualenv-clone                  0.5.7
WARNING: You are using pip version 21.2.3; however, version 21.3 is available.
You should consider upgrading via the 'C:\Users\Yuan\AppData\Local\Programs\Python\Python310\python.exe -m pip install --upgrade pip' command.


jupyter_env
cd C:\jupyter_env
pipenv shell --python C:\Users\Yuan\AppData\Local\Programs\Python\Python310\python.exe
or
pipenv shell --python 3.8
or
pipenv --python 3.8

pipenv shell
activate

# Where env was created
(jupyter_env-2FENnPD8) C:\jupyter_env>pipenv --venv
C:\Users\Yuan\.virtualenvs\jupyter_env-2FENnPD8



=================================================================================================================

C:\Users\Yuan>python -m venv C:\jupyter_env python=3.5
=================================================================================================================
```


```
https://pypi.org/project/pyenv-win/1.1.2/

Project description
pyenv for Windows
The pyenv is a great tool. I ported it to Windows. Some commands doesn't implemented, but wouldn't be a problem in basic use.

License: MIT GitHub issues open

Introduction
pyenv
pyenv-win does
Installation
How it works
How to get updates
FAQ
How to contribute
Bug Tracker and Support
License and Copyright
Author and Thanks
Introduction
The pyenv for python is a great tool, but it doesn't supports windowns platform directly, which was the same case in rbenv for ruby developers. After a bit of research and feedbacks from python developers, they loves to have such a feature for windows systems.

I got inspired from the pyenv issues for windows support, personally I too use mac and linux with beautiful pyenv, but in some companies they still use windows for there development. This library is to help windows users to manage multiple pythons.

Found a similar system for rbenv-win for ruby developers. This project was forked from rbenv-win and modified for pyenv. Some commands doesn't implemented, but wouldn't be a problem in basic use.

pyenv
pyenv is a simple python version management tool. It lets you easily switch between multiple versions of Python. It's simple, unobtrusive, and follows the UNIX tradition of single-purpose tools that do one thing well.

pyenv-win does
   commands    List all available pyenv commands
   local       Set or show the local application-specific Python version
   global      Set or show the global Python version
   shell       Set or show the shell-specific Python version
   install     Install a Python version using python-build
   uninstall   Uninstall a specific Python version
   rehash      Rehash pyenv shims (run this after installing executables)
   version     Show the current Python version and its origin
   versions    List all Python versions available to pyenv
   exec        Runs an executable by first preparing PATH so that the selected Python
Installation
Installing by pip: (To support existing python users)

For command prompt use following command pip install pyenv-win --target %USERPROFILE%/.pyenv (or)
For git bash or alternative use following command pip install pyenv-win --target $HOME/.pyenv
Add the following paths to your ENVIRONMENT PATH variable for accessing to pyenv command %USERPROFILE%\.pyenv\pyenv-win\bin;%USERPROFILE%\.pyenv\pyenv-win\shims; at the begining
ENVIRONMENT PATH :: My Computer -> Propertires -> Advanced system settings -> Advanced -> Environment Variables -> PATH
Open command prompt (new session) and type pyenv --version
You need to see current pyenv version. If you are getting an error go through the steps again still facing the issue open a ticket.
Type pyenv to see list of commands it support. More..
Installation is done hurray...!

Installing by downloading zip file:

Link: pyenv-win

Extract to your %USERPROFILE%/.pyenv/pyenv-win

Add the following paths to your ENVIRONMENT PATH variable for accessing to pyenv command %USERPROFILE%\.pyenv\pyenv-win\bin;%USERPROFILE%\.pyenv\pyenv-win\shims; at the begining

ENVIRONMENT PATH :: My Computer -> Propertires -> Advanced system settings -> Advanced -> Environment Variables -> PATH
Open command prompt (new session) and type pyenv --version

You need to see current pyenv version. If you are getting an error go through the steps again still facing the issue open a ticket.

Type pyenv to see list of commands it support. More..

Installation is done hurray...!

Installing by git:

Clone the repository to the user profile
git clone https://github.com/pyenv-win/pyenv-win.git %USERPROFILE%/.pyenv/pyenv-win

Add the following paths to your ENVIRONMENT PATH variable for accessing to pyenv command %USERPROFILE%\.pyenv\pyenv-win\bin;%USERPROFILE%\.pyenv\pyenv-win\shims; at the begining

ENVIRONMENT PATH :: My Computer -> Propertires -> Advanced system settings -> Advanced -> Environment Variables -> PATH
Open command prompt (new session) and type pyenv --version

You need to see current pyenv version. If you are getting an error go through the steps again still facing the issue open a ticket.

Type pyenv to see list of commands it support. More..

Installation is done hurray...!

How it works
To view list of python versions supported by pyenv windows. pyenv install -l
To install python version. pyenv install 3.5.2 Note: older version of python is msi file just click on next to install (no need of changing any options it in)
To set a python version as global version. pyenv global 3.5.2 Note: version needs to be installed
To set a python version as local version. pyenv local 3.5.2 you can give any version which you wanted to use to the project, this will be auto activated by entering to the folder not like other virtual env. to activate.
To uninstall any python version. pyenv uninstall 3.5.2
To know which python you are using and it's path pyenv version
To view all the python versions installed in this system pyenv versions
How to get updates
Installed via pip
Add pyenv-win installed path to easy_install.pth file which is located in site-package. Now pyenv-win is registered in pip
Get updates via pip pip install --upgrade pyenv-win
Installed via git
Go to the %USERPROFILE%/.pyenv/pyenv-win (which is your installed path) and type git pull
Installed via zip
Go to the path %USERPROFILE$/.pyenv/pyenv-win/ replace libexec and bin folder
FAQ
Question: Does pyenv for windows support python2?
Answer: Yes, We are supporting python2 from the version 2.0.1. We are supporting from 2.0.1 until the python.org officially removes.

Question: Does pyenv for windows support python3?
Answer: Yes, we are supporting python3 from the version 3.0. We are supporting from 3.0 until the python.org officially removes.

Question: I am getting an issue batch file cannot be found. while installing python, what to do?
Answer: You can ignore it. It's calling pyenv rehash command before creating the bat file in few devices.

Question: System is stuck while uninstalling the python version, what to do?
Answer: It's based on the system policies, you can manually uninstall by going to the path %USERPROFILE%/.pyenv/pyenv-win/install_cache/. I believe you know manual uninstallation. Please remove the site-package and scripts while uninstalling (mandatory). Double check the python version folder doesn't exist in the path %USERPROFILE%/.pyenv/pyenv-win/versions/ if exist please do remove it (mandatory).

Question: I installed pyenv-win using pip how to uninstall it?
Answer: Follow How to get updates in pip link and then pip uninstall pyenv-win

How to contribute
Fork the project & clone locally.
Create an upstream remote and sync your local copy before you branch.
Branch for each separate piece of work. It's a good practise to write test cases.
Do the work, write good commit messages, and read the CONTRIBUTING file if there is one.
Test the changes by running tests\test_install.bat and tests\test_uninstall.bat
Push to your origin repository.
Create a new Pull Request in GitHub.
Bug Tracker and Support
Please report any suggestions, bug reports, or annoyances with pyenv-win through the Github bug tracker.
License and Copyright
pyenv-win is licensed under MIT 2019

License: MIT

Author and Thanks
pyenv-win was developed by Kiran Kumar Kotari

```
