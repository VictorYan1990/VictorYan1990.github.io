---
layout: post
title:  "Python Project Setup from Scratch Using `venv` and `pip` in PyCharm"
date:   2023-12-10 21:46:26 -0500
categories: jekyll update
---
### Step 1: Install Python

1. **Download Python**:
   - Go to the [official Python website](https://www.python.org/downloads/).
   - Download the latest version of Python for Windows.

2. **Run the Installer**:
   - Open the downloaded file.
   - **Important**: Check the box that says **"Add Python X.X to PATH"**.
   - Click on "Install Now".

### Step 2: Create a New Project in PyCharm

1. **Open PyCharm**:
   - Start PyCharm on your laptop.

2. **Create a New Project**:
   - Choose **"File" > "New Project"**.

3. **Set Project Location**:
   - Navigate to `C:\Users\vicya\Repos`.
   - Create a new folder for your project, e.g., `MyProject`.
   - Select this folder as the project location.

4. **Configure Interpreter**:
   - In the "New Project" window, select the option to create a new virtual environment.
   - Choose the base Python interpreter you installed earlier.
   - Specify the location for the virtual environment, typically within your project folder.

5. **Create Project**:
   - Click "Create" to create your new project.

### Step 3: Work with Virtual Environment (venv)

1. **Activate venv**:
   - PyCharm automatically activates the virtual environment for your project.

2. **Install Packages with pip**:
   - To install a package, go to the terminal within PyCharm (usually at the bottom).
   - Type `pip install package_name`, replacing `package_name` with the name of the package you want to install.
   - Example: `pip install numpy`

### Step 4: Start Coding

1. **Create Python Files**:
   - Right-click on the project folder in PyCharm.
   - Select **"New" > "Python File"**.
   - Name your file, e.g., `main.py`.

2. **Write Your Code**:
   - Start coding in the newly created Python file.

### Step 5: Run Your Project

1. **Run the Script**:
   - Right-click on your Python file in PyCharm.
   - Select **"Run 'main.py'"** to execute your script.

### Additional Tips

- **Package Management**: To manage packages, use the `pip install`, `pip uninstall`, and `pip freeze` commands in the PyCharm terminal.
- **Requirements File**: To keep track of your project's dependencies, create a `requirements.txt` file by running `pip freeze > requirements.txt` in the terminal.
- **Update Python**: To update Python, download the newer version and repeat the installation steps. PyCharm should automatically detect the new version.
