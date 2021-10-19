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
=================================================================================================================
```
