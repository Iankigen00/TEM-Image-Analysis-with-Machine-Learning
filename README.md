# TEM-Image-Analysis-with-Machine-Learning

Utilizing AtomAI and Google Colab to analyze atomic-resolution TEM data, identify lattice defects, and simulate synthetic material datasets.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Google Colab](https://img.shields.io/badge/Google%20Colab-Ready-F9AB00)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-AtomAI-success)

## 📖 Project Overview

This repository bridges theoretical machine learning paradigms with practical implementations using AtomAI and experimental TEM datasets. It explores how computer vision can be leveraged to "see" and understand complex atomic phenomena in materials science.

### The Role of Computer Vision in Materials Science
Computer vision extracts information from electron microscopy to make critical discoveries:
*   **Processing:** Enhancing visuals to highlight atomic structures.
*   **Detection:** Identifying edges, shapes, and complex features.
*   **Recognition:** Classifying objects (e.g., distinguishing between different types of defects).

### Machine Learning Paradigms Utilized
1.  **Supervised Learning:** Training models using labeled data (e.g., identifying Mo adatoms or vacancies in MoS2 lattices). Highly accurate but requires extensive manual annotation.
2.  **Semi-Supervised Learning:** Combining a small amount of labeled data with a vast amount of unlabeled data using pseudo-labeling.
3.  **Unsupervised Learning:** Grouping and clustering unlabeled data to find hidden structural patterns.

### Modeling Real Imperfections
To build robust models without relying solely on hand-labeled data, we generate synthetic datasets that account for real-world TEM imperfections:
*   **Contamination:** Simulating artifacts from electron beams or polishing.
*   **Noise:** Adding realistic instrument noise or holder drift.
*   **Transformations:** Applying shear, rotation, and scaling.

---

## 🗂️ Repository Structure

### 📓 Google Colab Notebooks
These `.ipynb` files are fully compatible with Google Colab. Simply upload them to your Google Drive and open them with Colab to leverage cloud GPUs.
*   **`atomai_training_data-STL.ipynb`** & **`atomai_training_data-STLv2.ipynb`**: Core tutorials for preparing training data using AtomAI. Covers the simulation of training sets and formatting experimental inputs.
*   **`MoS2-Atom detection.ipynb`**: A practical implementation of supervised learning to identify pristine lattice sites and specific defects (Mo/S vacancies and adatoms) in MoS2 structures.
*   **`SingleImage-Nanoparticles-Colab.ipynb`**: A Colab-specific notebook focusing on extracting visual features, contour detection, and segmentation mapping for nanoparticle datasets.

### 📊 Datasets & Raw Images
*   **`2H-MoS2.npy`** & **`2H-MoS2.json`**: Experimental lattice images and atomic coordinate ground-truths for 2H-phase MoS2.
*   **`3R_0.npy`** & **`3R_0.json`**: Experimental images and coordinate annotations for 3R-phase materials.
*   **`0.png`**: Raw high-resolution image data utilized in the extraction and processing pipelines.

### 🧠 Synthetic Data & Trained Models
*   **`Synthetic_train_test.npz`**: A comprehensive archive of simulated training and testing data, infused with modeled imperfections (shear, rotation, noise) to train robust models. *(Note: Requires Git LFS due to file size)*.
*   **`Trained-Images.npz`**: Stored arrays containing model outputs, probability maps, or pre-trained network states for rapid deployment.

---

## 🚀 Getting Started with Google Colab

1. **Clone or Download:** Download the repository files to your local machine or Google Drive.
2. **Upload to Colab:** Go to [Google Colab](https://colab.research.google.com/), click "Upload", and select any of the `.ipynb` notebooks.
3. **Install Dependencies:** Inside the first cell of your Colab notebook, ensure AtomAI is installed by running:
   ```python
   !pip install git+[https://github.com/pycroscopy/atomai](https://github.com/pycroscopy/atomai)
