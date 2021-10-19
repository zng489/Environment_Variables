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

## Miniconda 
```
C:\Users\Yuan>conda create --name jupyter_conda python=3.8 -y
# The Environment created 'jupyter_conda'
C:\Users\Yuan>activate jupyter_conda
(jupyter_conda) C:\Users\Yuan>
(jupyter_conda) C:\Users\Yuan>pip install jupyter

http://127.0.0.1:8888/?token=280b5922018a3044e49bf8498e423628cdbb718bc58e2dfb
```

## Pyenv
```
where python
C:\Users\Yuan> where python
C:\Users\Yuan\AppData\Local\Programs\Python\Python310\python.exe
C:\Users\Yuan\AppData\Local\Microsoft\WindowsApps\python.exe

pyenv-win-master.zip
C:\python_v0\.pyenv\pyenv-win\bin
C:\python_v0\.pyenv\pyenv-win\shims

C:\Users\Yuan>pip install pipenv

pip list
C:\Users\Yuan> pip list

cd C:\jupyter_env> pipenv shell --python C:\Users\Yuan\AppData\Local\Programs\Python\Python310\python.exe

cd C:\jupyter_env
pipenv shell --python C:\Users\Yuan\AppData\Local\Programs\Python\Python310\python.exe

C:\python_v0\.pyenv\pyenv-win\versions\3.8.0

pip list

pipenv --venv

pipenv install pandas

pipenv shell

jupyter notebook
```
