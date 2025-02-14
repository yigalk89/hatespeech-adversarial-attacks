# Hatespeech Adversarial Attacks  

This repository contains code for the research project **"Adversarial Attacks on State-of-the-Art (SOTA) Hate Speech Detection Models."** The project investigates how adversarial perturbations impact the performance of leading hate speech detection models and explores methods to enhance model robustness.  

## Setup  

To ensure smooth execution of the notebooks, create a shortcut to the following Google Drive folder in your Drive’s top-level directory:  
[Project Data Folder](https://drive.google.com/drive/folders/1nIsH8rEUcUjNEC2bvTBRIdRhunaLa95A?usp=drive_link)  

## Notebook Descriptions  

### **Create_perturbed_anthro_data_set.ipynb**  
This notebook loads the **HateExplain** dataset and applies the [ANTHRO](https://github.com/lethaiq/perturbations-in-the-wild) framework to replace hateful words with semantically equivalent alternatives while preserving their meaning.  

### **perturbing_train_test_val_of_hateexplain.ipynb**  
This notebook utilizes the **Mixtral-8x7B-32768** model to perturb the HateExplain dataset while ensuring semantic consistency.  

### **Data_Cleaning.ipynb**  
This notebook extracts perturbed sentences from the Mixtral-8x7B-32768 model’s output and refines the dataset to reduce noise and improve clarity.  

### **different_models_evaluation.ipynb**  
This notebook evaluates the performance of the following hate speech detection models:  
- **Rationale2**  
- **RoBERTa Hate Speech**  
- **BERT HateExplain**  

The evaluation compares each model’s performance on the original **HateExplain** dataset against its perturbed version.  

### **Fine_tune_Bert_HateExplain.ipynb**  
After determining that the **BERT HateExplain** model experiences the most significant performance degradation due to perturbations, this notebook fine-tunes the model to improve its robustness against adversarial hate speech modifications.  
