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
```bash
conda create -n astra_curved 
conda activate astra_curved
```
### **2.  Install Astra Toolbox**
 ```bash
conda install -c wjpalenstijn/label/curved astra-toolbox
```

### **3. Clone and Install ODL From Correct Branch**
```bash
git clone https://github.com/wjp/odl.git curved
cd curved
pip install .
```
