# Interpretable Depression Diagnosis from Brain Imaging
TEAM_ID_2 / PROJECT_ID_2
## Overview
This repository contains two related projects for diagnosing depression using machine learning, showcasing a progression from synthetic to real data:

1. Synthetic Data Project ('Team_ID_2_ML.ipynb'): An initial implementation using manually generated synthetic MRI-like features to develop and test an interpretable ML pipeline.
2. Real Data Project ('Depression_Diagnosis.ipynb'): A refined model using real fMRI data from the Kaggle dataset "Depression Detection Using MRI" transitioning to practical application with enhanced preprocessing and a demo UI.

Both projects employ Logistic Regression, Decision Tree, and SVM models, with a focus on interpretability using feature importance and visualization.

## Installation
1. Clone the repository: `git clone https://github.com/pes2202401522-afk/ML_C_PES2UG24CS803_ADITHYA_C.git`
2. Install dependencies: `pip install -r requirements.txt` (create this file below).
3. For the Real Data Project:
   - Download the Kaggle dataset: [Depression Detection Using MRI](https://www.kaggle.com/datasets/anshumanprabhakar/depression-detection-using-mri) and place it in `data/raw/`.
4. Open the respective notebook (`Team_ID_2_ML.ipynb` or `Depression_Diagnosis.ipynb`) in Jupyter Notebook or Colab to run the pipeline.

## Project Structure
- `Team_ID_2_ML.ipynb`: Notebook for the synthetic data project, including data generation, feature selection, and model training.
- `Depression_Diagnosis.ipynb`: Main notebook for the real data project, with MRI preprocessing, modeling, and evaluation.
- `ui.py`: Streamlit app for demoing predictions using real MRI data.
- `data/processed/`: Processed CSV file (`processed_mri_data.csv`) with extracted features from real fMRI data.
- `figures/`: Visualization files (e.g., `decision_tree.png`, `confusion_matrix.png`) from the real data project.
- `model/`: Saved models and scaler (e.g., `lr_model.pkl`, `scaler.pkl`) from the real data project.

## Running the Projects
### Synthetic Data Project
1. Open `Team_ID_2_ML.ipynb` and run all cells sequentially.
2. The notebook generates synthetic data, trains models, and displays results (e.g., feature coefficients, tree visualization).

### Real Data Project
1. Execute `Depression_Diagnosis.ipynb` cells sequentially to preprocess real fMRI data, train models, and generate figures.
2. Run the UI:
   - Install Streamlit (`pip install streamlit`) and use ngrok or localtunnel:
     - **Ngrok**: Follow setup in notebook comments (requires auth token).
     - **Localtunnel**: `!streamlit run ui.py & npx localtunnel --port 8501` with IP password (fetch with `!curl ipv4.icanhazip.com`).
   3. Upload an MRI file to the UI for prediction.

## Dependencies
Create a `requirements.txt` file with:
numpy
pandas
scikit-learn
matplotlib
seaborn
nibabel
nilearn
torch
torchvision


## Demo
- The Streamlit UI (for the real data project) allows uploading MRI files to predict depression status and visualize top contributing features.
- The synthetic project outputs are viewable directly in the notebook.

## Development Progression
- **Synthetic Data Phase**: Developed an initial proof-of-concept with synthetic ROI intensities and labels, focusing on model interpretability.
- **Real Data Phase**: Enhanced the pipeline with real fMRI data preprocessing (using `nilearn`), atlas-based feature extraction, and a live demo, implemented in Google Colab.

## Notes
- Raw MRI data is not included; download from Kaggle for the real data project.
- The synthetic data project does not require external datasets.
- Contact: [adithyac8700@gmail.com] 


## Acknowledgments
- Kaggle community for the "Depression Detection Using MRI" dataset.
- Google Colab for free computational resources.
streamlit
joblib
