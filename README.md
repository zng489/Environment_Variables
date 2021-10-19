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
Microsoft Windows [Version 10.0.18363.418]
(c) 2019 Microsoft Corporation. All rights reserved.

C:\Users\Yuan>pyenv --version
PYENV variable is not set, recommended to set the variable.
pyenv 2.64.11

C:\Users\Yuan>pyenv install -l
:: [Info] ::  Mirror: https://www.python.org/ftp/python
2.4-win32
2.4.1-win32
2.4.2-win32
2.4.3c1-win32
2.4.3-win32
2.4.4-win32
2.5-win32
2.5
2.5.1-win32
2.5.1
2.5.2-win32
2.5.2
2.5.3c1-win32
2.5.3c1
2.5.3-win32
2.5.3
2.5.4-win32
2.5.4
2.6-win32
2.6
2.6.1-win32
2.6.1
2.6.2c1-win32
2.6.2c1
2.6.2-win32
2.6.2
2.6.3rc1-win32
2.6.3rc1
2.6.3-win32
2.6.3
2.6.4rc1-win32
2.6.4rc1
2.6.4rc2-win32
2.6.4rc2
2.6.4-win32
2.6.4
2.6.5rc1-win32
2.6.5rc1
2.6.5rc2-win32
2.6.5rc2
2.6.5-win32
2.6.5
2.6.6rc1-win32
2.6.6rc1
2.6.6rc2-win32
2.6.6rc2
2.6.6-win32
2.6.6
2.7-win32
2.7
2.7.1rc1-win32
2.7.1rc1
2.7.1-win32
2.7.1
2.7.2rc1-win32
2.7.2rc1
2.7.2-win32
2.7.2
2.7.3rc1-win32
2.7.3rc1
2.7.3rc2-win32
2.7.3rc2
2.7.3-win32
2.7.3
2.7.4rc1-win32
2.7.4rc1
2.7.4-win32
2.7.4
2.7.5-win32
2.7.5
2.7.6rc1-win32
2.7.6rc1
2.7.6-win32
2.7.6
2.7.7rc1-win32
2.7.7rc1
2.7.7-win32
2.7.7
2.7.8-win32
2.7.8
2.7.9rc1-win32
2.7.9rc1
2.7.9-win32
2.7.9
2.7.10rc1-win32
2.7.10rc1
2.7.10-win32
2.7.10
2.7.11rc1-win32
2.7.11rc1
2.7.11-win32
2.7.11
2.7.12rc1-win32
2.7.12rc1
2.7.12-win32
2.7.12
2.7.13rc1-win32
2.7.13rc1
2.7.13-win32
2.7.13
2.7.14rc1-win32
2.7.14rc1
2.7.14-win32
2.7.14
2.7.15rc1-win32
2.7.15rc1
2.7.15-win32
2.7.15
2.7.16rc1-win32
2.7.16rc1
2.7.16-win32
2.7.16
2.7.17rc1-win32
2.7.17rc1
2.7.17-win32
2.7.17
2.7.18rc1-win32
2.7.18rc1
2.7.18-win32
2.7.18
3.0a1-win32
3.0a1
3.0a2
3.0a3-win32
3.0a3
3.0a4-win32
3.0a4
3.0a5-win32
3.0a5
3.0b1-win32
3.0b1
3.0b2-win32
3.0b2
3.0b3-win32
3.0b3
3.0rc1-win32
3.0rc1
3.0rc2-win32
3.0rc2
3.0rc3-win32
3.0rc3
3.0-win32
3.0
3.0.1-win32
3.0.1
3.1-win32
3.1
3.1.1-win32
3.1.1
3.1.2rc1-win32
3.1.2rc1
3.1.2-win32
3.1.2
3.1.3rc1-win32
3.1.3rc1
3.1.3-win32
3.1.3
3.1.4rc1-win32
3.1.4rc1
3.1.4-win32
3.1.4
3.2-win32
3.2
3.2.1-win32
3.2.1
3.2.2-win32
3.2.2
3.2.3-win32
3.2.3
3.2.4-win32
3.2.4
3.2.5-win32
3.2.5
3.3.0-win32
3.3.0
3.3.1-win32
3.3.1
3.3.2-win32
3.3.2
3.3.3-win32
3.3.3
3.3.4rc1-win32
3.3.4rc1
3.3.4-win32
3.3.4
3.3.5rc1-win32
3.3.5rc1
3.3.5rc2-win32
3.3.5rc2
3.3.5-win32
3.3.5
3.4.0a1-win32
3.4.0a1
3.4.0a2-win32
3.4.0a2
3.4.0a3-win32
3.4.0a3
3.4.0a4-win32
3.4.0a4
3.4.0b1-win32
3.4.0b1
3.4.0b2-win32
3.4.0b2
3.4.0b3-win32
3.4.0b3
3.4.0rc1-win32
3.4.0rc1
3.4.0rc2-win32
3.4.0rc2
3.4.0rc3-win32
3.4.0rc3
3.4.0-win32
3.4.0
3.4.1rc1-win32
3.4.1rc1
3.4.1-win32
3.4.1
3.4.2rc1-win32
3.4.2rc1
3.4.2-win32
3.4.2
3.4.3rc1-win32
3.4.3rc1
3.4.3-win32
3.4.3
3.4.4rc1-win32
3.4.4rc1
3.4.4-win32
3.4.4
3.5.0a1-win32
3.5.0a1
3.5.0a2-win32
3.5.0a2
3.5.0a3-win32
3.5.0a3
3.5.0a4-win32
3.5.0a4
3.5.0a5-win32
3.5.0a5
3.5.0b1-win32
3.5.0b1
3.5.0b2-win32
3.5.0b2
3.5.0b3-win32
3.5.0b3
3.5.0b4-win32
3.5.0b4
3.5.0rc1-win32
3.5.0rc1
3.5.0rc2-win32
3.5.0rc2
3.5.0rc3-win32
3.5.0rc3
3.5.0rc4-win32
3.5.0rc4
3.5.0-win32
3.5.0
3.5.1rc1-win32
3.5.1rc1
3.5.1-win32
3.5.1
3.5.2rc1-win32
3.5.2rc1
3.5.2-win32
3.5.2
3.5.3rc1-win32
3.5.3rc1
3.5.3-win32
3.5.3
3.5.4rc1-win32
3.5.4rc1
3.5.4-win32
3.5.4
3.6.0a1-win32
3.6.0a1
3.6.0a2-win32
3.6.0a2
3.6.0a3-win32
3.6.0a3
3.6.0a4-win32
3.6.0a4
3.6.0b1-win32
3.6.0b1
3.6.0b2-win32
3.6.0b2
3.6.0b3-win32
3.6.0b3
3.6.0b4-win32
3.6.0b4
3.6.0rc1-win32
3.6.0rc1
3.6.0rc2-win32
3.6.0rc2
3.6.0-win32
3.6.0
3.6.1rc1-win32
3.6.1rc1
3.6.1-win32
3.6.1
3.6.2rc1-win32
3.6.2rc1
3.6.2rc2-win32
3.6.2rc2
3.6.2-win32
3.6.2
3.6.3rc1-win32
3.6.3rc1
3.6.3-win32
3.6.3
3.6.4rc1-win32
3.6.4rc1
3.6.4-win32
3.6.4
3.6.5rc1-win32
3.6.5rc1
3.6.5-win32
3.6.5
3.6.6rc1-win32
3.6.6rc1
3.6.6-win32
3.6.6
3.6.7rc1-win32
3.6.7rc1
3.6.7rc2-win32
3.6.7rc2
3.6.7-win32
3.6.7
3.6.8rc1-win32
3.6.8rc1
3.6.8-win32
3.6.8
3.7.0a1-win32
3.7.0a1
3.7.0a2-win32
3.7.0a2
3.7.0a3-win32
3.7.0a3
3.7.0a4-win32
3.7.0a4
3.7.0b1-win32
3.7.0b1
3.7.0b2-win32
3.7.0b2
3.7.0b3-win32
3.7.0b3
3.7.0b4-win32
3.7.0b4
3.7.0b5-win32
3.7.0b5
3.7.0rc1-win32
3.7.0rc1
3.7.0-win32
3.7.0
3.7.1rc1-win32
3.7.1rc1
3.7.1rc2-win32
3.7.1rc2
3.7.1-win32
3.7.1
3.7.2rc1-win32
3.7.2rc1
3.7.2-win32
3.7.2
3.7.3rc1-win32
3.7.3rc1
3.7.3-win32
3.7.3
3.7.4rc1-win32
3.7.4rc1
3.7.4rc2-win32
3.7.4rc2
3.7.4-win32
3.7.4
3.7.5rc1-win32
3.7.5rc1
3.7.5-win32
3.7.5
3.7.6rc1-win32
3.7.6rc1
3.7.6-win32
3.7.6
3.7.7rc1-win32
3.7.7rc1
3.7.7-win32
3.7.7
3.7.8rc1-win32
3.7.8rc1
3.7.8-win32
3.7.8
3.7.9-win32
3.7.9
3.8.0a1-win32
3.8.0a1
3.8.0a2-win32
3.8.0a2
3.8.0a3-win32
3.8.0a3
3.8.0a4-win32
3.8.0a4
3.8.0b1-win32
3.8.0b1
3.8.0b2-win32
3.8.0b2
3.8.0b3-win32
3.8.0b3
3.8.0b4-win32
3.8.0b4
3.8.0rc1-win32
3.8.0rc1
3.8.0-win32
3.8.0
3.8.1rc1-win32
3.8.1rc1
3.8.1-win32
3.8.1
3.8.2rc1-win32
3.8.2rc1
3.8.2rc2-win32
3.8.2rc2
3.8.2-win32
3.8.2
3.8.3rc1-win32
3.8.3rc1
3.8.3-win32
3.8.3
3.8.4rc1-win32
3.8.4rc1
3.8.4-win32
3.8.4
3.8.5-win32
3.8.5
3.8.6rc1-win32
3.8.6rc1
3.8.6-win32
3.8.6
3.8.7rc1-win32
3.8.7rc1
3.8.7-win32
3.8.7
3.8.8rc1-win32
3.8.8rc1
3.8.8-win32
3.8.8
3.8.9-win32
3.8.9
3.8.10-win32
3.8.10
3.9.0a1-win32
3.9.0a1
3.9.0a2-win32
3.9.0a2
3.9.0a3-win32
3.9.0a3
3.9.0a4-win32
3.9.0a4
3.9.0a5-win32
3.9.0a5
3.9.0a6-win32
3.9.0a6
3.9.0b1-win32
3.9.0b1
3.9.0b2-win32
3.9.0b2
3.9.0b3-win32
3.9.0b3
3.9.0b4-win32
3.9.0b4
3.9.0b5-win32
3.9.0b5
3.9.0rc1-win32
3.9.0rc1
3.9.0rc2-win32
3.9.0rc2
3.9.0-win32
3.9.0
3.9.1rc1-win32
3.9.1rc1
3.9.1-win32
3.9.1
3.9.2rc1-win32
3.9.2rc1
3.9.2-win32
3.9.2
3.9.3-win32
3.9.3
3.9.4-win32
3.9.4
3.9.5-win32
3.9.5
3.9.6-win32
3.9.6
3.10.0a1-win32
3.10.0a1
3.10.0a2-win32
3.10.0a2
3.10.0a3-win32
3.10.0a3
3.10.0a4-win32
3.10.0a4
3.10.0a5-win32
3.10.0a5
3.10.0a6-win32
3.10.0a6
3.10.0a7-win32
3.10.0a7
3.10.0b1-win32
3.10.0b1
3.10.0b2-win32
3.10.0b2
3.10.0b3-win32
3.10.0b3
pypy3.6-v7.3.3-win32
pypy3.7-v7.3.3-win32
pypy3.7-v7.3.4

C:\Users\Yuan>pyenv install --list
:: [Info] ::  Mirror: https://www.python.org/ftp/python
2.4-win32
2.4.1-win32
2.4.2-win32
2.4.3c1-win32
2.4.3-win32
2.4.4-win32
2.5-win32
2.5
2.5.1-win32
2.5.1
2.5.2-win32
2.5.2
2.5.3c1-win32
2.5.3c1
2.5.3-win32
2.5.3
2.5.4-win32
2.5.4
2.6-win32
2.6
2.6.1-win32
2.6.1
2.6.2c1-win32
2.6.2c1
2.6.2-win32
2.6.2
2.6.3rc1-win32
2.6.3rc1
2.6.3-win32
2.6.3
2.6.4rc1-win32
2.6.4rc1
2.6.4rc2-win32
2.6.4rc2
2.6.4-win32
2.6.4
2.6.5rc1-win32
2.6.5rc1
2.6.5rc2-win32
2.6.5rc2
2.6.5-win32
2.6.5
2.6.6rc1-win32
2.6.6rc1
2.6.6rc2-win32
2.6.6rc2
2.6.6-win32
2.6.6
2.7-win32
2.7
2.7.1rc1-win32
2.7.1rc1
2.7.1-win32
2.7.1
2.7.2rc1-win32
2.7.2rc1
2.7.2-win32
2.7.2
2.7.3rc1-win32
2.7.3rc1
2.7.3rc2-win32
2.7.3rc2
2.7.3-win32
2.7.3
2.7.4rc1-win32
2.7.4rc1
2.7.4-win32
2.7.4
2.7.5-win32
2.7.5
2.7.6rc1-win32
2.7.6rc1
2.7.6-win32
2.7.6
2.7.7rc1-win32
2.7.7rc1
2.7.7-win32
2.7.7
2.7.8-win32
2.7.8
2.7.9rc1-win32
2.7.9rc1
2.7.9-win32
2.7.9
2.7.10rc1-win32
2.7.10rc1
2.7.10-win32
2.7.10
2.7.11rc1-win32
2.7.11rc1
2.7.11-win32
2.7.11
2.7.12rc1-win32
2.7.12rc1
2.7.12-win32
2.7.12
2.7.13rc1-win32
2.7.13rc1
2.7.13-win32
2.7.13
2.7.14rc1-win32
2.7.14rc1
2.7.14-win32
2.7.14
2.7.15rc1-win32
2.7.15rc1
2.7.15-win32
2.7.15
2.7.16rc1-win32
2.7.16rc1
2.7.16-win32
2.7.16
2.7.17rc1-win32
2.7.17rc1
2.7.17-win32
2.7.17
2.7.18rc1-win32
2.7.18rc1
2.7.18-win32
2.7.18
3.0a1-win32
3.0a1
3.0a2
3.0a3-win32
3.0a3
3.0a4-win32
3.0a4
3.0a5-win32
3.0a5
3.0b1-win32
3.0b1
3.0b2-win32
3.0b2
3.0b3-win32
3.0b3
3.0rc1-win32
3.0rc1
3.0rc2-win32
3.0rc2
3.0rc3-win32
3.0rc3
3.0-win32
3.0
3.0.1-win32
3.0.1
3.1-win32
3.1
3.1.1-win32
3.1.1
3.1.2rc1-win32
3.1.2rc1
3.1.2-win32
3.1.2
3.1.3rc1-win32
3.1.3rc1
3.1.3-win32
3.1.3
3.1.4rc1-win32
3.1.4rc1
3.1.4-win32
3.1.4
3.2-win32
3.2
3.2.1-win32
3.2.1
3.2.2-win32
3.2.2
3.2.3-win32
3.2.3
3.2.4-win32
3.2.4
3.2.5-win32
3.2.5
3.3.0-win32
3.3.0
3.3.1-win32
3.3.1
3.3.2-win32
3.3.2
3.3.3-win32
3.3.3
3.3.4rc1-win32
3.3.4rc1
3.3.4-win32
3.3.4
3.3.5rc1-win32
3.3.5rc1
3.3.5rc2-win32
3.3.5rc2
3.3.5-win32
3.3.5
3.4.0a1-win32
3.4.0a1
3.4.0a2-win32
3.4.0a2
3.4.0a3-win32
3.4.0a3
3.4.0a4-win32
3.4.0a4
3.4.0b1-win32
3.4.0b1
3.4.0b2-win32
3.4.0b2
3.4.0b3-win32
3.4.0b3
3.4.0rc1-win32
3.4.0rc1
3.4.0rc2-win32
3.4.0rc2
3.4.0rc3-win32
3.4.0rc3
3.4.0-win32
3.4.0
3.4.1rc1-win32
3.4.1rc1
3.4.1-win32
3.4.1
3.4.2rc1-win32
3.4.2rc1
3.4.2-win32
3.4.2
3.4.3rc1-win32
3.4.3rc1
3.4.3-win32
3.4.3
3.4.4rc1-win32
3.4.4rc1
3.4.4-win32
3.4.4
3.5.0a1-win32
3.5.0a1
3.5.0a2-win32
3.5.0a2
3.5.0a3-win32
3.5.0a3
3.5.0a4-win32
3.5.0a4
3.5.0a5-win32
3.5.0a5
3.5.0b1-win32
3.5.0b1
3.5.0b2-win32
3.5.0b2
3.5.0b3-win32
3.5.0b3
3.5.0b4-win32
3.5.0b4
3.5.0rc1-win32
3.5.0rc1
3.5.0rc2-win32
3.5.0rc2
3.5.0rc3-win32
3.5.0rc3
3.5.0rc4-win32
3.5.0rc4
3.5.0-win32
3.5.0
3.5.1rc1-win32
3.5.1rc1
3.5.1-win32
3.5.1
3.5.2rc1-win32
3.5.2rc1
3.5.2-win32
3.5.2
3.5.3rc1-win32
3.5.3rc1
3.5.3-win32
3.5.3
3.5.4rc1-win32
3.5.4rc1
3.5.4-win32
3.5.4
3.6.0a1-win32
3.6.0a1
3.6.0a2-win32
3.6.0a2
3.6.0a3-win32
3.6.0a3
3.6.0a4-win32
3.6.0a4
3.6.0b1-win32
3.6.0b1
3.6.0b2-win32
3.6.0b2
3.6.0b3-win32
3.6.0b3
3.6.0b4-win32
3.6.0b4
3.6.0rc1-win32
3.6.0rc1
3.6.0rc2-win32
3.6.0rc2
3.6.0-win32
3.6.0
3.6.1rc1-win32
3.6.1rc1
3.6.1-win32
3.6.1
3.6.2rc1-win32
3.6.2rc1
3.6.2rc2-win32
3.6.2rc2
3.6.2-win32
3.6.2
3.6.3rc1-win32
3.6.3rc1
3.6.3-win32
3.6.3
3.6.4rc1-win32
3.6.4rc1
3.6.4-win32
3.6.4
3.6.5rc1-win32
3.6.5rc1
3.6.5-win32
3.6.5
3.6.6rc1-win32
3.6.6rc1
3.6.6-win32
3.6.6
3.6.7rc1-win32
3.6.7rc1
3.6.7rc2-win32
3.6.7rc2
3.6.7-win32
3.6.7
3.6.8rc1-win32
3.6.8rc1
3.6.8-win32
3.6.8
3.7.0a1-win32
3.7.0a1
3.7.0a2-win32
3.7.0a2
3.7.0a3-win32
3.7.0a3
3.7.0a4-win32
3.7.0a4
3.7.0b1-win32
3.7.0b1
3.7.0b2-win32
3.7.0b2
3.7.0b3-win32
3.7.0b3
3.7.0b4-win32
3.7.0b4
3.7.0b5-win32
3.7.0b5
3.7.0rc1-win32
3.7.0rc1
3.7.0-win32
3.7.0
3.7.1rc1-win32
3.7.1rc1
3.7.1rc2-win32
3.7.1rc2
3.7.1-win32
3.7.1
3.7.2rc1-win32
3.7.2rc1
3.7.2-win32
3.7.2
3.7.3rc1-win32
3.7.3rc1
3.7.3-win32
3.7.3
3.7.4rc1-win32
3.7.4rc1
3.7.4rc2-win32
3.7.4rc2
3.7.4-win32
3.7.4
3.7.5rc1-win32
3.7.5rc1
3.7.5-win32
3.7.5
3.7.6rc1-win32
3.7.6rc1
3.7.6-win32
3.7.6
3.7.7rc1-win32
3.7.7rc1
3.7.7-win32
3.7.7
3.7.8rc1-win32
3.7.8rc1
3.7.8-win32
3.7.8
3.7.9-win32
3.7.9
3.8.0a1-win32
3.8.0a1
3.8.0a2-win32
3.8.0a2
3.8.0a3-win32
3.8.0a3
3.8.0a4-win32
3.8.0a4
3.8.0b1-win32
3.8.0b1
3.8.0b2-win32
3.8.0b2
3.8.0b3-win32
3.8.0b3
3.8.0b4-win32
3.8.0b4
3.8.0rc1-win32
3.8.0rc1
3.8.0-win32
3.8.0
3.8.1rc1-win32
3.8.1rc1
3.8.1-win32
3.8.1
3.8.2rc1-win32
3.8.2rc1
3.8.2rc2-win32
3.8.2rc2
3.8.2-win32
3.8.2
3.8.3rc1-win32
3.8.3rc1
3.8.3-win32
3.8.3
3.8.4rc1-win32
3.8.4rc1
3.8.4-win32
3.8.4
3.8.5-win32
3.8.5
3.8.6rc1-win32
3.8.6rc1
3.8.6-win32
3.8.6
3.8.7rc1-win32
3.8.7rc1
3.8.7-win32
3.8.7
3.8.8rc1-win32
3.8.8rc1
3.8.8-win32
3.8.8
3.8.9-win32
3.8.9
3.8.10-win32
3.8.10
3.9.0a1-win32
3.9.0a1
3.9.0a2-win32
3.9.0a2
3.9.0a3-win32
3.9.0a3
3.9.0a4-win32
3.9.0a4
3.9.0a5-win32
3.9.0a5
3.9.0a6-win32
3.9.0a6
3.9.0b1-win32
3.9.0b1
3.9.0b2-win32
3.9.0b2
3.9.0b3-win32
3.9.0b3
3.9.0b4-win32
3.9.0b4
3.9.0b5-win32
3.9.0b5
3.9.0rc1-win32
3.9.0rc1
3.9.0rc2-win32
3.9.0rc2
3.9.0-win32
3.9.0
3.9.1rc1-win32
3.9.1rc1
3.9.1-win32
3.9.1
3.9.2rc1-win32
3.9.2rc1
3.9.2-win32
3.9.2
3.9.3-win32
3.9.3
3.9.4-win32
3.9.4
3.9.5-win32
3.9.5
3.9.6-win32
3.9.6
3.10.0a1-win32
3.10.0a1
3.10.0a2-win32
3.10.0a2
3.10.0a3-win32
3.10.0a3
3.10.0a4-win32
3.10.0a4
3.10.0a5-win32
3.10.0a5
3.10.0a6-win32
3.10.0a6
3.10.0a7-win32
3.10.0a7
3.10.0b1-win32
3.10.0b1
3.10.0b2-win32
3.10.0b2
3.10.0b3-win32
3.10.0b3
pypy3.6-v7.3.3-win32
pypy3.7-v7.3.3-win32
pypy3.7-v7.3.4

C:\Users\Yuan>cd C:\jupyter_code

C:\jupyter_code>pyenv install --list
:: [Info] ::  Mirror: https://www.python.org/ftp/python
2.4-win32
2.4.1-win32
2.4.2-win32
2.4.3c1-win32
2.4.3-win32
2.4.4-win32
2.5-win32
2.5
2.5.1-win32
2.5.1
2.5.2-win32
2.5.2
2.5.3c1-win32
2.5.3c1
2.5.3-win32
2.5.3
2.5.4-win32
2.5.4
2.6-win32
2.6
2.6.1-win32
2.6.1
2.6.2c1-win32
2.6.2c1
2.6.2-win32
2.6.2
2.6.3rc1-win32
2.6.3rc1
2.6.3-win32
2.6.3
2.6.4rc1-win32
2.6.4rc1
2.6.4rc2-win32
2.6.4rc2
2.6.4-win32
2.6.4
2.6.5rc1-win32
2.6.5rc1
2.6.5rc2-win32
2.6.5rc2
2.6.5-win32
2.6.5
2.6.6rc1-win32
2.6.6rc1
2.6.6rc2-win32
2.6.6rc2
2.6.6-win32
2.6.6
2.7-win32
2.7
2.7.1rc1-win32
2.7.1rc1
2.7.1-win32
2.7.1
2.7.2rc1-win32
2.7.2rc1
2.7.2-win32
2.7.2
2.7.3rc1-win32
2.7.3rc1
2.7.3rc2-win32
2.7.3rc2
2.7.3-win32
2.7.3
2.7.4rc1-win32
2.7.4rc1
2.7.4-win32
2.7.4
2.7.5-win32
2.7.5
2.7.6rc1-win32
2.7.6rc1
2.7.6-win32
2.7.6
2.7.7rc1-win32
2.7.7rc1
2.7.7-win32
2.7.7
2.7.8-win32
2.7.8
2.7.9rc1-win32
2.7.9rc1
2.7.9-win32
2.7.9
2.7.10rc1-win32
2.7.10rc1
2.7.10-win32
2.7.10
2.7.11rc1-win32
2.7.11rc1
2.7.11-win32
2.7.11
2.7.12rc1-win32
2.7.12rc1
2.7.12-win32
2.7.12
2.7.13rc1-win32
2.7.13rc1
2.7.13-win32
2.7.13
2.7.14rc1-win32
2.7.14rc1
2.7.14-win32
2.7.14
2.7.15rc1-win32
2.7.15rc1
2.7.15-win32
2.7.15
2.7.16rc1-win32
2.7.16rc1
2.7.16-win32
2.7.16
2.7.17rc1-win32
2.7.17rc1
2.7.17-win32
2.7.17
2.7.18rc1-win32
2.7.18rc1
2.7.18-win32
2.7.18
3.0a1-win32
3.0a1
3.0a2
3.0a3-win32
3.0a3
3.0a4-win32
3.0a4
3.0a5-win32
3.0a5
3.0b1-win32
3.0b1
3.0b2-win32
3.0b2
3.0b3-win32
3.0b3
3.0rc1-win32
3.0rc1
3.0rc2-win32
3.0rc2
3.0rc3-win32
3.0rc3
3.0-win32
3.0
3.0.1-win32
3.0.1
3.1-win32
3.1
3.1.1-win32
3.1.1
3.1.2rc1-win32
3.1.2rc1
3.1.2-win32
3.1.2
3.1.3rc1-win32
3.1.3rc1
3.1.3-win32
3.1.3
3.1.4rc1-win32
3.1.4rc1
3.1.4-win32
3.1.4
3.2-win32
3.2
3.2.1-win32
3.2.1
3.2.2-win32
3.2.2
3.2.3-win32
3.2.3
3.2.4-win32
3.2.4
3.2.5-win32
3.2.5
3.3.0-win32
3.3.0
3.3.1-win32
3.3.1
3.3.2-win32
3.3.2
3.3.3-win32
3.3.3
3.3.4rc1-win32
3.3.4rc1
3.3.4-win32
3.3.4
3.3.5rc1-win32
3.3.5rc1
3.3.5rc2-win32
3.3.5rc2
3.3.5-win32
3.3.5
3.4.0a1-win32
3.4.0a1
3.4.0a2-win32
3.4.0a2
3.4.0a3-win32
3.4.0a3
3.4.0a4-win32
3.4.0a4
3.4.0b1-win32
3.4.0b1
3.4.0b2-win32
3.4.0b2
3.4.0b3-win32
3.4.0b3
3.4.0rc1-win32
3.4.0rc1
3.4.0rc2-win32
3.4.0rc2
3.4.0rc3-win32
3.4.0rc3
3.4.0-win32
3.4.0
3.4.1rc1-win32
3.4.1rc1
3.4.1-win32
3.4.1
3.4.2rc1-win32
3.4.2rc1
3.4.2-win32
3.4.2
3.4.3rc1-win32
3.4.3rc1
3.4.3-win32
3.4.3
3.4.4rc1-win32
3.4.4rc1
3.4.4-win32
3.4.4
3.5.0a1-win32
3.5.0a1
3.5.0a2-win32
3.5.0a2
3.5.0a3-win32
3.5.0a3
3.5.0a4-win32
3.5.0a4
3.5.0a5-win32
3.5.0a5
3.5.0b1-win32
3.5.0b1
3.5.0b2-win32
3.5.0b2
3.5.0b3-win32
3.5.0b3
3.5.0b4-win32
3.5.0b4
3.5.0rc1-win32
3.5.0rc1
3.5.0rc2-win32
3.5.0rc2
3.5.0rc3-win32
3.5.0rc3
3.5.0rc4-win32
3.5.0rc4
3.5.0-win32
3.5.0
3.5.1rc1-win32
3.5.1rc1
3.5.1-win32
3.5.1
3.5.2rc1-win32
3.5.2rc1
3.5.2-win32
3.5.2
3.5.3rc1-win32
3.5.3rc1
3.5.3-win32
3.5.3
3.5.4rc1-win32
3.5.4rc1
3.5.4-win32
3.5.4
3.6.0a1-win32
3.6.0a1
3.6.0a2-win32
3.6.0a2
3.6.0a3-win32
3.6.0a3
3.6.0a4-win32
3.6.0a4
3.6.0b1-win32
3.6.0b1
3.6.0b2-win32
3.6.0b2
3.6.0b3-win32
3.6.0b3
3.6.0b4-win32
3.6.0b4
3.6.0rc1-win32
3.6.0rc1
3.6.0rc2-win32
3.6.0rc2
3.6.0-win32
3.6.0
3.6.1rc1-win32
3.6.1rc1
3.6.1-win32
3.6.1
3.6.2rc1-win32
3.6.2rc1
3.6.2rc2-win32
3.6.2rc2
3.6.2-win32
3.6.2
3.6.3rc1-win32
3.6.3rc1
3.6.3-win32
3.6.3
3.6.4rc1-win32
3.6.4rc1
3.6.4-win32
3.6.4
3.6.5rc1-win32
3.6.5rc1
3.6.5-win32
3.6.5
3.6.6rc1-win32
3.6.6rc1
3.6.6-win32
3.6.6
3.6.7rc1-win32
3.6.7rc1
3.6.7rc2-win32
3.6.7rc2
3.6.7-win32
3.6.7
3.6.8rc1-win32
3.6.8rc1
3.6.8-win32
3.6.8
3.7.0a1-win32
3.7.0a1
3.7.0a2-win32
3.7.0a2
3.7.0a3-win32
3.7.0a3
3.7.0a4-win32
3.7.0a4
3.7.0b1-win32
3.7.0b1
3.7.0b2-win32
3.7.0b2
3.7.0b3-win32
3.7.0b3
3.7.0b4-win32
3.7.0b4
3.7.0b5-win32
3.7.0b5
3.7.0rc1-win32
3.7.0rc1
3.7.0-win32
3.7.0
3.7.1rc1-win32
3.7.1rc1
3.7.1rc2-win32
3.7.1rc2
3.7.1-win32
3.7.1
3.7.2rc1-win32
3.7.2rc1
3.7.2-win32
3.7.2
3.7.3rc1-win32
3.7.3rc1
3.7.3-win32
3.7.3
3.7.4rc1-win32
3.7.4rc1
3.7.4rc2-win32
3.7.4rc2
3.7.4-win32
3.7.4
3.7.5rc1-win32
3.7.5rc1
3.7.5-win32
3.7.5
3.7.6rc1-win32
3.7.6rc1
3.7.6-win32
3.7.6
3.7.7rc1-win32
3.7.7rc1
3.7.7-win32
3.7.7
3.7.8rc1-win32
3.7.8rc1
3.7.8-win32
3.7.8
3.7.9-win32
3.7.9
3.8.0a1-win32
3.8.0a1
3.8.0a2-win32
3.8.0a2
3.8.0a3-win32
3.8.0a3
3.8.0a4-win32
3.8.0a4
3.8.0b1-win32
3.8.0b1
3.8.0b2-win32
3.8.0b2
3.8.0b3-win32
3.8.0b3
3.8.0b4-win32
3.8.0b4
3.8.0rc1-win32
3.8.0rc1
3.8.0-win32
3.8.0
3.8.1rc1-win32
3.8.1rc1
3.8.1-win32
3.8.1
3.8.2rc1-win32
3.8.2rc1
3.8.2rc2-win32
3.8.2rc2
3.8.2-win32
3.8.2
3.8.3rc1-win32
3.8.3rc1
3.8.3-win32
3.8.3
3.8.4rc1-win32
3.8.4rc1
3.8.4-win32
3.8.4
3.8.5-win32
3.8.5
3.8.6rc1-win32
3.8.6rc1
3.8.6-win32
3.8.6
3.8.7rc1-win32
3.8.7rc1
3.8.7-win32
3.8.7
3.8.8rc1-win32
3.8.8rc1
3.8.8-win32
3.8.8
3.8.9-win32
3.8.9
3.8.10-win32
3.8.10
3.9.0a1-win32
3.9.0a1
3.9.0a2-win32
3.9.0a2
3.9.0a3-win32
3.9.0a3
3.9.0a4-win32
3.9.0a4
3.9.0a5-win32
3.9.0a5
3.9.0a6-win32
3.9.0a6
3.9.0b1-win32
3.9.0b1
3.9.0b2-win32
3.9.0b2
3.9.0b3-win32
3.9.0b3
3.9.0b4-win32
3.9.0b4
3.9.0b5-win32
3.9.0b5
3.9.0rc1-win32
3.9.0rc1
3.9.0rc2-win32
3.9.0rc2
3.9.0-win32
3.9.0
3.9.1rc1-win32
3.9.1rc1
3.9.1-win32
3.9.1
3.9.2rc1-win32
3.9.2rc1
3.9.2-win32
3.9.2
3.9.3-win32
3.9.3
3.9.4-win32
3.9.4
3.9.5-win32
3.9.5
3.9.6-win32
3.9.6
3.10.0a1-win32
3.10.0a1
3.10.0a2-win32
3.10.0a2
3.10.0a3-win32
3.10.0a3
3.10.0a4-win32
3.10.0a4
3.10.0a5-win32
3.10.0a5
3.10.0a6-win32
3.10.0a6
3.10.0a7-win32
3.10.0a7
3.10.0b1-win32
3.10.0b1
3.10.0b2-win32
3.10.0b2
3.10.0b3-win32
3.10.0b3
pypy3.6-v7.3.3-win32
pypy3.7-v7.3.3-win32
pypy3.7-v7.3.4

C:\jupyter_code>pyenv install -v 3.8
:: [Info] ::  Mirror: https://www.python.org/ftp/python
pyenv-install: definition not found: -v

See all available versions with `pyenv install --list'.

C:\jupyter_code>pyenv install -v 3.8.0
:: [Info] ::  Mirror: https://www.python.org/ftp/python
pyenv-install: definition not found: -v

See all available versions with `pyenv install --list'.

C:\jupyter_code>pyenv install 3.8.0
:: [Info] ::  Mirror: https://www.python.org/ftp/python
:: [Downloading] ::  3.8.0 ...
:: [Downloading] ::  From https://www.python.org/ftp/python/3.8.0/python-3.8.0-amd64-webinstall.exe
:: [Downloading] ::  To   C:\pyenv_win\.pyenv\pyenv-win\install_cache\python-3.8.0-amd64-webinstall.exe
:: [Installing] ::  3.8.0 ...
:: [Info] :: completed! 3.8.0

C:\jupyter_code>
```

## Miniconda 

```
C:\Users\Yuan>conda create --name jupyter_conda python=3.8 -y
# The Environment created 'jupyter_conda'
C:\Users\Yuan>activate jupyter_conda
(jupyter_conda) C:\Users\Yuan>
(jupyter_conda) C:\Users\Yuan>pip install jupyter
```



# Foobar

Foobar is a Python library for dealing with word pluralization.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install foobar
```

## Usage

```python
import foobar

# returns 'words'
foobar.pluralize('word')

# returns 'geese'
foobar.pluralize('goose')

# returns 'phenomenon'
foobar.singularize('phenomena')
```
