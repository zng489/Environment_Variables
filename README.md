# Environment_Variables
C:\Users\Yuan\miniconda3\envs\jupyter_conda
```
=================================================================================================================
python -m venv myenv
python -m venv myenv python=3.6
=================================================================================================================
conda create -n myenv
conda create -n myenv python=3.6
=================================================================================================================
```

# Miniconda 
```
=================================================================================================================

Download >> https://docs.conda.io/en/latest/miniconda.html

Step 1 >> Latest - Conda 4.10.3 Python 3.9.5 released July 21, 2021

Step 2 >> Platform	Name	SHA256 hash Windows	Miniconda3 Windows 64-bit	
b33797064593ab2229a0135dc69001bea05cb56a20c2f243b1231213642e260a

------------------------------------------------------------------------------------------------------------------
where conda
where python

C:\Users\Yuan>
>> conda create --name jupyter_conda_python_3.8 python=3.8 -y

>> conda activate jupyter_conda_python_3.8

>> conda deactivate

C:\Users\Yuan>
>> conda activate jupyter_conda_python_3.8

(jupyter_conda_python_3.8) C:\Users\Yuan>
>> pip install jupyter

(jupyter_conda_python_3.8) C:\Users\Yuan>
>> jupyter notebook
>> conda env list
********************************************************************************************************************
C:\Users\Yuan>activate jupyter_v_2.7
(jupyter_v_2.7) C:\Users\Yuan>python
********************************************************************************************************************

=================================================================================================================
pip install -r /path/to/requirements.txt


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


## Activating Anaconda Environment in VsCode
```
Command Prompt

settings.json
{
    "python.pythonPath":"C:\\Users\\Yuan\\miniconda3\\envs\\jupyter_conda\\python.exe"
}
```

# Opening jupyter in VSC
```
=================================================================================================================
1 - Installing and download miniconda
2 - Creating the environment and pip jupyter
3 - Opening the VSC and install the extesion for ipynb file
4 - pip uninstall if necessary!!!
=================================================================================================================
```
