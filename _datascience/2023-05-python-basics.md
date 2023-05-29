---
title: "Python Basics"
excerpt: "Short description for basics of python programming"
collection: datascience
---

# Check the Python Version
````python
import sys
print(sys.version)
````
# Installing Python Packages in JupyterNotebook
We need to be careful on installing python packages in the JupyterNotebook. Fundamentally the problem is usually rooted in the fact that the **Jupyter kernels are disconnected from Jupyter's shell**; in other words, the installer points to a different Python version than is being used in the notebook. In the simplest contexts this issue does not arise, but when it does, debugging the problem requires knowledge of the intricacies of the operating system, the intricacies of Python package installation, and the intricacies of Jupyter itself. In other words, the Jupyter notebook, like all abstractions, is leaky.<br><br>
Following the instruction from the [reference](https://jakevdp.github.io/blog/2017/12/05/installing-python-packages-from-jupyter/), <br><br>
``!{sys.executable} -m pip install <python-package>``
<br>
System settings about float type
````python
sys.float_info
````
<h3 id="convert">Converting from one object type to a different object type</h3>
````python
float(2)

# Casting 1.1 to integer will result in loss of information
int(1.1)

# Convert a string into an integer
int('1')

# Convert an integer to a string
str(1)

# Convert True to float
float(True)
````
<br>
Integer division operation expression
````python
25 // 3
````




The JupyterNotebook with very basic information about Python codes is [here](https://abinashpun.github.io/datascience_files/Basic_Python_Notes.ipynb)
