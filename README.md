# Humour Styles Recognition Dataset and Model Repository

This repository contains the dataset and code implementations for the research paper titled "A Two-Model Approach for Humour Style Recognition". The research aims to automatically recognise different styles of humour, including self-enhancing, self-deprecating, affiliative, aggressive humour, and neutral (not humourous).

## Datasets
The dataset was compiled from various websites and labeled based on the provided definitions, tags, or categories. Each instance consists of a joke or non-humourous text, along with its corresponding style label. More details about the dataset can be found in our paper. 

The **dataset** folder contains a new annotated dataset of 1,463 instances across the four humour styles and Non-humourous text with a dataset_ReadME file explaining each dataset file. 

### Files
1. **'Humour_style.xlsx'**: Dataset containing humour samples annotated with with five classes. 
The 'Humour_style.xlsx' dataset labels are:
- Self-enhancing : 0
- Self-deprecating: 1
- Affiliative: 2
- Aggressive: 3
- Neutral: 4

2. **'Humour_style_4classes.xlsx'**: This file was used to train the 4-class model of the two-model approach. The jokes are the same as those in the Humour_style.xlsx file, but the labels were adjusted to 4 classes. 
The 'Humour_style_4classes.xlsx' dataset labels are:
- Self-enhancing : 0
- Self-deprecating: 1
- Affiliative/Aggressive: 2
- Neutral: 3

3. **'af_ag_train.xlsx'** and **'af_ag_test.xlsx'**: Dataset containing only affiliative and aggressive humour samples. The 'af_ag_train.xlsx' is the training dataset used for the binary model while the 'af_ag_test.xlsx' is the test dataset. 
The 'af_ag_train.xlsx' and 'af_ag_test.xlsx' dataset labels are:
- Affiliative: 0
- Aggressive: 1

4. **Note:** All files contain the same jokes, as they are subsets of the Humour_style.xlsx file.

### Data Format
The datasets are provided in excel or CSV format with the following columns:
- **'JOKES'**: Text smaples to be classified
- **'LABELS'**: Annotation indicating the humour style of each text sample

## Models 
### Description
The repository includes code for training and evaluating the machine learning models for humour style recognition. It covers various models, including classical machine learning classifiers, text embedding models, and transformer-based models like DistilBERT.

### Files
- **data_preprocessing.py**: Utility functions for data preprocessing 
- **naive_bayes_model.ipynb**: Implementation of the Naive Bayes classifier.
- **embedding_model.ipynb**: Implementation of the Random Forest and XGBoost classifier with various text embeddings (GTE, BGE, ALI, MRL, UAE, MUL).
- **distilBERT_pre_trained_model.ipynb**: Implementation of the DistilBERT model for humour style classification.
- **statistical_test.ipynb**: Implementation of the Wilcoxon signed-rank test  used to compare the single-model and two-model approaches, determining the statistical significance of the performance differences between these approaches.
- **requirements.txt**: List of Python dependencies

Each Model file contains implementation for the single-model (five-class classification) approach and the Two-model approach (four-class and Binary classification) as described in the paper. 

## Usage
- Clone the repository:
```bash
git clone https://github.com/MaryKenneth/Two_Model_Humour_Style.git
```

- Install the required dependencies:    
```bash
pip install -r requirements.txt
```
- Run the code for the desired model(s) by executing the corresponding Jupyter file(s).

# References
If you use this dataset or code in your research, please cite the following paper:

