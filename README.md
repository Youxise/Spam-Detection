# Spam Email Detection

## Project Overview
This project aims to build a machine learning model capable of classifying emails as spam or non-spam. The process involves importing labeled emails, cleaning the text data, encoding it for machine learning models, and training different classification algorithms to achieve optimal performance.

## Table of Contents
1. [Installation](#installation)
2. [Data Importation](#data-importation)
3. [Data Preprocessing](#data-preprocessing)
4. [Model Building & Evaluation](#model-building--evaluation)
5. [Results](#results)
6. [License](#license)

## Installation
To run this project, ensure you have the required dependencies installed. Use the following command to install them:
```bash
pip install numpy pandas matplotlib seaborn nltk scikit-learn
```

Additionally, if using Google Colab, mount Google Drive:
```python
from google.colab import drive
drive.mount("/content/gdrive")
```

## Data Importation
A function is implemented to traverse files within a directory in Google Drive and import labeled emails (spam & ham).

## Data Preprocessing
Various preprocessing steps are applied to clean and standardize the text data:
- **Lowercasing**: Convert all text to lowercase.
- **HTML Tag Removal**: Remove unnecessary HTML tags.
- **Normalization**: Convert URLs, email addresses, numbers, and dollar signs to generic tokens.
- **Tokenization & Lemmatization**: Extract word roots.
- **Removal of Non-Words**: Eliminate punctuation, spaces, and tabs.
- **Feature Selection**: Select the most frequently occurring words.
- **Mapping & Transformation**: Assign unique numbers to words and count occurrences per email.

## Model Building & Evaluation
- **Pipeline**: A pipeline groups multiple transformations to optimize the data processing workflow.
- **Standard Scaler**: Standardizes data to ensure models converge efficiently.
- **Cross Validation**: Splits data into K folds, training models multiple times to enhance reliability.
- **Stratified K-Fold**: Ensures balanced class distribution during training.
- **Grid Search**: Tunes hyperparameters to find the best model configuration.

### Classification Models Used
The following algorithms are trained and evaluated:
- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)
- Neural Networks

## Results
The performance of each model is assessed using:
- Confusion Matrices
- Accuracy, Precision, Recall, F1-score, ROC Curve

## License
This project is licensed under the MIT License.

**Author**: Youxise
