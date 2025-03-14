# Git setup
Download and install git from [here](https://git-scm.com/downloads).

Once setup, clone the `python-training` repository using the command
```
git clone https://github.com/hd-code-git/python-training.git
```

# Python Development Setup

This guide outlines the steps to set up a Python development environment, including installing Python, pip, virtualenv, and configuring a Jupyter kernel within the virtual environment.

## Python Installation

1. **Download Python:** Download the appropriate Python installer for your operating system from the [Python website](https://www.python.org/).  The recommended version to install is 3.13.2.

2. **Verify Installation:** Open a terminal or command prompt and run `python3 --version` to verify that Python is installed correctly.  The output should display the installed Python version.

## Pip Installation

Pip is usually installed alongside Python. Verify its installation by running `pip3 --version` in your terminal.

## Virtual Environment Setup

1. **Install virtualenv:** Open your terminal and execute `pip3 install virtualenv`.  This command installs the virtualenv package, which allows you to create isolated Python environments.

2. **Create a Virtual Environment:** Navigate to your repoistory's home directory using the `cd python-training` command. Once in the repository's home directory, create a new virtual environment by running `python3 -m venv <environment_name>`, replacing `<environment_name>` with your desired name for the environment (e.g., `my_env`).

3. **Activate the Virtual Environment:**  
    - **Linux/macOS:** Activate the environment using the command `source <environment_name>/bin/activate`.  For example, if your environment is named `my_env`, the command would be `source my_env/bin/activate`.
    - **Windows:** Activate the environment using `<environment_name>\Scripts\activate`.  For example: `my_env\Scripts\activate`.
    You'll know the environment is activated when the environment name appears in parentheses at the beginning of your terminal prompt.

3. **Install required Python Packages:** On your terminal, execute `pip3 install -r requirements.txt` from the repository's home folder.


## Jupyter Kernel

1. **Install Jupyter:** With your virtual environment activated, run `pip install jupyter`.

2. **Add Virtual Environment as a Kernel:** Run the following command to add your virtual environment as a kernel for Jupyter:
   `python -m ipykernel install --user --name=<environment_name>` (replace `<environment_name>` with your virtual environment name). This makes the environment's Python interpreter and installed packages available to Jupyter notebooks.

3. **Start Jupyter Notebook:**  Run `jupyter notebook` to launch Jupyter. When you create a new `.ipynb` notebook or launch an existing one, select the kernel with the same name as your virtual environment from the kernel selection menu.  This ensures your notebook uses the isolated environment you've set up.


## Working within your environment
Any subsequent installations of packages using `pip install` should be done with the virtual environment active. This confines the packages to that specific environment, preventing conflicts with other projects.  To deactivate the virtual environment, simply type `deactivate` in the terminal.

## Introduction to Python Notebook
Open the notebook named `Introduction to Python.ipynb` and use `shift+enter` to execute each cell. At any time, to clear outputs in the notebook, you can do `Edit -> Clear Outputs of All Cells`.

For further guidance on jupyter notebooks, you can refer to this [link](https://docs.jupyter.org/en/latest/).