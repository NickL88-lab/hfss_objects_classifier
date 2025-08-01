# HFSS Objects Classifier (Demonstrator)

This repository hosts a preliminary version of a deep learning-based classifier for electromagnetic simulation geometries, specifically targeting models exported from **HFSS (High Frequency Structure Simulator)**.

## Status: Demonstrator Only

**This is an early-stage demonstrator.**  
At the moment, the classifier has been trained and tested using only **two object classes**:

- `horn` (horn antennas)  
- `riflettore` (reflectors)

It is **not a production-ready tool**, but rather a proof of concept aimed at exploring automatic classification of geometric objects from simulation data.

---

## Project Goals

The main objective of this project is to investigate whether simple 3D geometry descriptors, possibly derived from HFSS-generated models, can be effectively used to train neural networks for classification purposes.

In particular, the long-term goal is to support **less experienced users** of HFSS by:

- Automatically recognizing 3D objects within the HFSS modeler  
- Suggesting appropriate **boundary conditions**, **hybrid region types**, and **solver configurations** based on the recognized object type  
- Reducing the likelihood of simulation setup errors and improving productivity during the design phase

This system could eventually act as a smart assistant to guide users in setting up correct and efficient electromagnetic simulations.

<img width="1182" height="715" alt="download (1)" src="https://github.com/user-attachments/assets/d26e577d-9fb9-4839-87a6-d5f931b9026b" />

---

## Notebook Overview

A key part of the repository is a **Jupyter Notebook** that demonstrates the full classification pipeline, including:

- Importing and organizing geometric features extracted from HFSS objects  
- Preprocessing and normalization of input data  
- Building a simple feed-forward neural network using PyTorch  
- Training the network on a small labeled dataset of two classes (`horn`, `riflettore`)  
- Evaluating classification performance using accuracy metrics and confusion matrices  
- Visualizing the training process and results

The model was trained using **Google Colab**, which provides free GPU acceleration and a convenient environment for experimentation.

---

## Structure

The repository currently contains:

- Scripts for preprocessing HFSS models  
- A basic neural network implementation for classification  
- Example datasets with labeled objects (`horn` and `riflettore`)  
- Notebooks and helper functions for training and evaluation

---

## Getting Started

Clone the repository:

```bash
git clone https://github.com/NickL88-lab/hfss_objects_classifier.git
cd hfss_objects_classifier
```

---

## Contributions & Feedback
Since this is a demonstrator, feedback and ideas for expansion or improvements are very welcome. Feel free to open issues or fork the project.

---

## License
This project is released under the MIT License.

