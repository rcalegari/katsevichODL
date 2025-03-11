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

```bash
conda create -n astra_curved python=3.9
conda activate astra_curved
conda install -c wjpalenstijn/label/curved astra-toolbox
pip install numpy==1.19.5
git clone https://github.com/wjp/odl.git astra_cyclone_binding
cd astra_cyclone_binding
pip install .
