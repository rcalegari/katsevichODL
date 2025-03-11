# KatsevichODL

## Overview
This repository implements the **Katsevich reconstruction algorithm** using the **Operator Discretization Library (ODL)** and **ASTRA Toolbox**. The Katsevich algorithm is a theoretically exact method for **helical cone-beam computed tomography (CT)**.

## Features
- **Katsevich reconstruction algorithm** implemented within the ODL framework.
- **Integration with ASTRA Toolbox** for efficient forward and back projections.
- **Compatible with helical CT scan geometries**.
- **Easily customizable** for different scanner configurations.

## Installation
To set up the environment and install dependencies, follow the [Installation Guide](#installation).

### **1. Create and Activate the Conda Environment**
Note that ODL uses some deprecated methods which are not compatible with python versions beyond 3.9.
```bash
conda create -n astra_curved python=3.9
conda activate astra_curved
```
### **2.  Install Astra Toolbox**
 ```bash
conda install -c wjpalenstijn/label/curved astra-toolbox
```
### **3. Install correct version of numPy**
```bash
conda uninstall numpy
conda install numpy=1.19.5
```
This is the compatible version to python=3.9.

### **4. Clone and Install ODL**
```bash
git clone https://github.com/wjp/odl.git astra_cyclone_binding
cd astra_cyclone_binding
grep -rl "np.object" . | xargs sed -i 's/np.object/object/g'
pip install .
```
### **5. Verify Installation**
Check that ASTRA and ODL are installed correctly:
```bash
python -c "import astra; print(astra.__version__)"
python -c "import odl; print(odl.__version__)"
```
If everything went right, this should return numpy=2.1.3 and odl=1.0.0.dev0.
