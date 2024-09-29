# **Mortality Prediction in ICU - TCN and BiGRU Deep Learning Framework**

## **Project Overview**
This project presents a deep learning framework for predicting ICU mortality using multivariate time series classification. The framework leverages **Temporal Convolutional Networks (TCNs)** and **Bidirectional Gated Recurrent Units (BiGRUs)** to capture complex temporal dependencies in ICU patient data, while addressing challenges such as missing values using **Generative Adversarial Networks (GANs)** for imputation.

## **Key Features**
- **Missing Value Imputation**: Uses GANs to handle missing data in the Electronic Health Records (EHR) dataset.
- **Time-Series Classification**: Utilizes TCNs and BiGRUs to model temporal dependencies.
- **Dataset Used**: MIMIC-III, a publicly available dataset containing ICU patient records.

## **Installation**

### **Dependencies:**
- Python 3.x
- TensorFlow
- Pandas
- NumPy
- scikit-learn
- tcn (custom library for Temporal Convolutional Networks)

## **Dataset**
The project uses the MIMIC-III dataset, which includes over 40,000 patient records from the ICU. To access this dataset, you must apply for permission via MIT and Beth Israel Deaconess Medical Center's Institutional Review Boards (IRBs).

# **Usage**
**Data Preprocessing**
- Impute Missing Values: The dataset contains missing values which are handled using a GAN-based approach.
Input: data01.csv (raw data)
Output: complete_dataset.csv (imputed dataset)
- Normalization: Perform Rolling Window Scaling on the time-series data to preserve temporal relationships during scaling.
 
**Model Training**
- Model Architecture: Combines TCN layers for temporal analysis and BiGRU layers for capturing bidirectional dependencies.
- Training Process:
Split the dataset into training and testing sets.
Train the model using binary cross-entropy loss and Adam optimizer.
Save the best model based on validation performance.
## **Evaluation**
Metrics used for model evaluation:

- Accuracy
- Precision
- Recall
- F1 Score
- Area Under the Curve (AUC)
