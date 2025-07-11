# FYP2
K-MEANS CLUSTERING FOR ECG WITH EXPLAINABLE AI

===========

K-MEANS CLUSTERING FOR ECG CLASSIFICATION WITH XAI
---------------------------------------------------

This project applies **K-Means Clustering** on ECG data from the **MIT-BIH Arrhythmia Database**, and explains the clustering results using **Explainable AI (XAI)** methods such as SHAP and LIME.

=================================================
1. REQUIRED TOOLS & ENVIRONMENT SETUP
=================================================

Python Version:
---------------
- Python 3.9 or newer (recommended: Python 3.10)

Installation Options:
---------------------
- [Anaconda (recommended)](https://www.anaconda.com/products/distribution)
  OR
- Download Python from the official site: https://www.python.org/downloads/

Create Virtual Environment (if not using Anaconda):

---------------------------------------------------
python -m venv venv
source venv/bin/activate      # (Linux/macOS)
venv\Scripts\activate.bat     # (Windows)

=================================================

2. REQUIRED PYTHON LIBRARIES
Install the necessary libraries using pip:

pip install numpy pandas matplotlib seaborn scikit-learn neurokit2 pywt shap lime
If you use Anaconda, you can create an environment and install with:

conda create -n ecg-xai python=3.10
conda activate ecg-xai
pip install numpy pandas matplotlib seaborn scikit-learn neurokit2 pywt shap lime

=================================================

3. HOW TO GET THE DATASET
This project uses the MIT-BIH Arrhythmia Database.

You can download it from PhysioNet:
👉 https://physionet.org/content/mitdb/1.0.0/

Steps:
Visit the link above.

Download the .dat, .hea, and .atr files (at least 10 records for testing).

Place them in a folder named data/ inside the same directory as your notebook.

Alternatively, you can use the WFDB Python library to download records:

pip install wfdb
Then run in a Python script:

import wfdb
wfdb.dl_database('mitdb', dl_dir='data/')

=================================================

4. HOW TO RUN THE NOTEBOOK
Launch Jupyter Notebook:

jupyter notebook
Open the file:

k-means-clustering.ipynb
Execute all cells sequentially to:

Load and preprocess ECG signals.

Extract features using NeuroKit2 and wavelet transforms.

Perform clustering with K-Means.

Apply XAI techniques (SHAP and LIME) to interpret the results.

=================================================

5. OUTPUT FILES
Extracted features will be saved as .csv files.

SHAP and LIME visualizations will be shown in notebook output cells.
