# Python Development Setup

This guide outlines the steps to set up a Python development environment, including installing Python, pip, virtualenv, and configuring a Jupyter kernel within the virtual environment.

## Python Installation

1. **Download Python:** Download the appropriate Python installer for your operating system from the [Python website](https://www.python.org/).  Ensure you select the correct version (e.g., Python 3.9). During installation, check the box to add Python to your system's PATH environment variable. This makes it easier to run Python from the command line.

2. **Verify Installation:** Open a terminal or command prompt and run `python --version` or `python3 --version` (depending on your installation) to verify that Python is installed correctly.  The output should display the installed Python version.

## Pip Installation

Pip is usually installed alongside Python. Verify its installation by running `pip --version` or `pip3 --version` in your terminal. If pip isn't installed, consult the Python documentation on how to install pip for your specific operating system.

## Virtual Environment Setup

1. **Install virtualenv:** Open your terminal and execute `pip install virtualenv` or `pip3 install virtualenv`.  This command installs the virtualenv package, which allows you to create isolated Python environments.

2. **Create a Virtual Environment:** Navigate to your project directory using the `cd` command. Once in the project directory, create a new virtual environment by running `python -m venv <environment_name>`, replacing `<environment_name>` with your desired name for the environment (e.g., `venv`, `.venv`).

3. **Activate the Virtual Environment:**  
    - **Linux/macOS:** Activate the environment using the command `source <environment_name>/bin/activate`.  For example, if your environment is named `venv`, the command would be `source venv/bin/activate`.
    - **Windows:** Activate the environment using `<environment_name>\Scripts\activate`.  For example: `venv\Scripts\activate`.
    You'll know the environment is activated when the environment name appears in parentheses at the beginning of your terminal prompt.


## Jupyter Kernel

1. **Install Jupyter:** With your virtual environment activated, run `pip install jupyter`.

2. **Add Virtual Environment as a Kernel:** Run the following command to add your virtual environment as a kernel for Jupyter:
   `python -m ipykernel install --user --name=<environment_name>` (replace `<environment_name>` with your virtual environment name). This makes the environment's Python interpreter and installed packages available to Jupyter notebooks.

3. **Start Jupyter Notebook:**  Run `jupyter notebook` to launch Jupyter. When you create a new `.ipynb` notebook or launch an existing one, select the kernel with the same name as your virtual environment from the kernel selection menu.  This ensures your notebook uses the isolated environment you've set up.


## Working within your environment
Any subsequent installations of packages using `pip install` should be done with the virtual environment active. This confines the packages to that specific environment, preventing conflicts with other projects.  To deactivate the virtual environment, simply type `deactivate` in the terminal.