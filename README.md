# QOSF-Screening-Tasks
This repository contains the submission of screening tasks for QOSF mentorship program, submitted in the name of Santhosh G S.


# Setting up the environment
The notebooks in this repository were ran on IBM quantum lab, where all the necessary packages are pre-installed. So, we have to just code and run. That it!

But, there are few steps to be done before you run these notebooks on your local machine. Below, are the steps needed to be performed on your local machine before running the notebooks, to reproduce similar results.

## 1. Creating a python virtual environment

Create a directory to work on your projects
```
mkdir Qiskit-projects
```
Create a python3 hidden source folder
```
python3 -m venv .virt-source
```
Change the python source directory to the one you created in the previous step
```
source .virt-source/bin/activate
```

## 2. Installing the package

Install the Qiskit package
```
pip install qiskit
```
If the packages were installed correctly, you can run ``pip list`` to see the active packages in your virtual environment.

## 3. Configuring the package

### 1. Setting up default drawer to Matplotlib

The default backend for `QuantumCircuit.draw()` or `qiskit.visualization.circuit_drawer()` is the text backend. However, depending on your local environment you may want to change these defaults to something better suited for your use case. This is done with the user config file. By default the user config file should be located in ``~/.qiskit/`` and is the ``settings.conf`` file.

IBM Quantum Lab uses default circuit drawer as Matplotlib. To reproduce visualizations as given in notebook create a settings.conf file (usually found in ~/.qiskit/) with contents:

```
[default]
circuit_drawer = mpl
```

### 2. Setting up default image type to svg

Optionally, you can add the following line of code to the `ipython_kernel_config.py` file (usually found in `~/.ipython/profile_default/`) to set the default image format from PNG to the more scaleable SVG format:

```
c.InlineBackend.figure_format = 'svg'
```

Aaand that's it for now. You can go ahead and run your projects or the notebooks from this github repo inside this repository.

What's stoppin you, go ahead and have funn !

[References](https://qiskit.org/documentation/getting_started.html)
