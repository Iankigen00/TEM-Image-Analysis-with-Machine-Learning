# TEM-Image-Analysis-with-Machine-Learning

Utilizing AtomAI and Google Colab to analyze atomic-resolution TEM data, identify lattice defects, and simulate synthetic material datasets.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-F9AB00)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-AtomAI-success)[cite: 8]

## 📖 Project Overview

This repository bridges theoretical machine learning paradigms with practical implementations using AtomAI and experimental TEM datasets.[cite: 8] It explores how computer vision can be leveraged to "see" and understand complex atomic phenomena in materials science.[cite: 8]

### The Role of Computer Vision in Materials Science[cite: 8]
Computer vision extracts information from electron microscopy to make critical discoveries:[cite: 8]
*   **Processing:** Enhancing visuals to highlight atomic structures.[cite: 8]
*   **Detection:** Identifying edges, shapes, and complex features.[cite: 8]
*   **Recognition:** Classifying objects (e.g., distinguishing between different types of defects).[cite: 8]

### Machine Learning Paradigms Utilized[cite: 8]
1.  **Supervised Learning:** Training models using labeled data (e.g., identifying Mo adatoms or vacancies in MoS2 lattices).[cite: 8] Highly accurate but requires extensive manual annotation.[cite: 8]
2.  **Semi-Supervised Learning:** Combining a small amount of labeled data with a vast amount of unlabeled data using pseudo-labeling.[cite: 8]
3.  **Unsupervised Learning:** Grouping and clustering unlabeled data to find hidden structural patterns.[cite: 8]

### Modeling Real Imperfections[cite: 8]
To build robust models without relying solely on hand-labeled data, we generate synthetic datasets that account for real-world TEM imperfections:[cite: 8]
*   **Contamination:** Simulating artifacts from electron beams or polishing.[cite: 8]
*   **Noise:** Adding realistic instrument noise or holder drift.[cite: 8]
*   **Transformations:** Applying shear, rotation, and scaling.[cite: 8]

---

## 🗂️ Repository Structure

### 📓 Google Colab Notebooks
These `.ipynb` files are fully compatible with Google Colab. Simply upload them to your Google Drive and open them with Colab to leverage cloud GPUs.
*   **`atomai_training_data-STL.ipynb`** & **`atomai_training_data-STLv2.ipynb`**: Core tutorials for preparing training data using AtomAI.[cite: 8] Covers the simulation of training sets and formatting experimental inputs.[cite: 8]
*   **`MoS2-Atom detection.ipynb`**: A practical implementation of supervised learning to identify pristine lattice sites and specific defects (Mo/S vacancies and adatoms) in MoS2 structures.[cite: 8]
*   **`SingleImage-Nanoparticles-Colab.ipynb`**: A Colab-specific notebook focusing on extracting visual features, contour detection, and segmentation mapping for nanoparticle datasets.[cite: 8]

### 📊 Datasets & Raw Images
*   **`2H-MoS2.npy`** & **`2H-MoS2.json`**: Experimental lattice images and atomic coordinate ground-truths for 2H-phase MoS2.[cite: 8]
*   **`3R_0.npy`** & **`3R_0.json`**: Experimental images and coordinate annotations for 3R-phase materials.[cite: 8]
*   **`0.png`**: Raw high-resolution image data utilized in the extraction and processing pipelines.[cite: 8]

### 🧠 Synthetic Data & Trained Models
*   **`Synthetic_train_test.npz`**: A comprehensive archive of simulated training and testing data, infused with modeled imperfections (shear, rotation, noise) to train robust models.[cite: 8] *(Note: Requires Git LFS due to file size)*.[cite: 8]
*   **`Trained-Images.npz`**: Stored arrays containing model outputs, probability maps, or pre-trained network states for rapid deployment.[cite: 8]

---

## 🚀 Getting Started with Google Colab

1. **Clone or Download:** Download the repository files to your local machine or Google Drive.
2. **Upload to Colab:** Go to [Google Colab](https://colab.research.google.com/), click "Upload", and select any of the `.ipynb` notebooks.
3. **Install Dependencies:** Inside the first cell of your Colab notebook, ensure AtomAI is installed by running:
   ```python
   !pip install git+[https://github.com/pycroscopy/atomai](https://github.com/pycroscopy/atomai)