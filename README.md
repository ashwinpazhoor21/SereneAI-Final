# Bioactivity and Compound Data Analysis Using NVIDIA BioNeMo, ChEMBL, and PubChem

## 🧪 Project Overview
This project aims to develop a **machine learning model** that predicts **bioactivity outcomes** based on compound properties and receptor interactions. We integrate **bioactivity data from ChEMBL** and **molecular properties from PubChem**, with model training powered by **NVIDIA’s BioNeMo framework**. 

The focus is on **serotonin and GABA receptors**, which are critical targets in **neurological drug discovery**. This project demonstrates the potential of **AI-driven insights** to advance pharmaceutical research.

---

## ✨ Features
1. **Data Collection from ChEMBL:**
   - Uses the **ChEMBL API** to retrieve bioactivity data.
   - Focus on **serotonin (CHEMBL233)** and **GABA receptors**.
   - Extracts metrics like **IC50 values** for drug activity evaluation.

2. **Data Augmentation with PubChem:**
   - Uses **PubChemPy** to fetch molecular descriptors:
     - **Molecular weight**
     - **LogP (lipophilicity)**
     - **Hydrogen bond donor/acceptor counts**
   - Enriches bioactivity data with chemical properties.

3. **Data Preprocessing:**
   - **Feature Scaling**: Standardizes numerical data for stability during training.
   - **Label Encoding**: Converts bioactivity values to model-compatible labels.
   - **Missing Value Handling**: Ensures clean and complete datasets.

4. **Model Training with NVIDIA NeMo:**
   - Leverages **BioNeMo API (Palmyra-Med-70B)** to generate predictions.
   - Locally trains a **Multi-Layer Perceptron (MLP)** with PyTorch/NeMo.
   - Supports **binary classification** of bioactivity outcomes.

5. **Model Evaluation:**
   - **Accuracy metrics** to assess model performance.
   - **Comparison of predictions** between local models and BioNeMo API results.

6. **Model Saving and Reusability:**
   - Saves trained models as `.pth` (PyTorch) and `.nemo` (NeMo) files.
   - Enables seamless **deployment and reuse** via BioNeMo API.

7. **Visualization:**
   - **Training loss plot** for tracking model convergence.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+
- NVIDIA NGC API Key (for BioNeMo API access)
- Libraries:
  ```bash
  pip install openai torch pandas scikit-learn nemo_toolkit requests pubchempy
