# Casting Defect with Logistic Regression
Logistic regression model for defect detection in casting product images.

I created this project to test my knowledge on what i learned from ML Specialization by Andrew NG

## Problem
Some of casting parts are deffective and some of them are non-deffective. Goal is to make model classify casting part is deffective or not.

## Dataset
Source: - [Casting_512x512](https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product)

## Approach
1. First i import libraries we need and load the data
2. When loading data i use HOG approach. HOG can detect defects related to our data since deffects are related to shape of casting parts we have and load data using gray scale since HOG uses it like this.
3. Then i observe properties of data i have
4. Since the number of non-deffective and deffective are different, i use stratify to split them 80/20 proportionally
5. Then i use Pipeline so i dont need to use StandardScaler everytime, instead Pipe does it for me
6. I used GridSearch CV so it can automatically test and choose Regularization parameter automatically
7. Then i train the model
8. And lastly evaluate the results

## Results

### Example image (non-deffective)
![Example image (non-deffective)](/results/non-defective_image.png)

### Number of non-deffective and deffective
![Number of non-deffective and deffective](/results/comparison.png)

### Accuracy, F1 Score, Recall and Precision

| Metric | Value |
|--------|-------|
| Model Accuracy | 91.54% |
| Best Regularization (C) | 0.1 |
| Best F1 Score (cross-validated) | 93.46% |
 
| Class          | Precision | Recall | F1-score | Support |
|----------------|-----------|--------|----------|---------|
| non-deffective | 0.87      | 0.92   | 0.90     | 104     |
| deffective     | 0.95      | 0.91   | 0.93     | 156     |
| **accuracy**   |           |        | 0.92     | 260     |
| **macro avg**  | 0.91      | 0.92   | 0.91     | 260     |
| **weighted avg** | 0.92    | 0.92   | 0.92     | 260     |

### Confusion Matrix
![Confusion Matrix](/results/confusion_matrix.png)


## Setup instruction
1. Download dataset i referenced above
2. Unzip and add it to data/ folder
3. Open new terminal inside project (can be done with 'Ctrl' + 'Shift' + '`')
4. Write 'pip install -r requirements.txt'

## Progress Log
 
| Date | Commit |
|------|--------|
| 6 July | Initializing the Project |
| 6 July | Added Logistic Regression model with HOG features and GridSearchCV |
| 6 July | Restart Kernel -> Run All |
| 6 July | Added Markdown Cells |
| 6 July | Finalized the Project by finishing README |
| 8 July | Adding My Linear Regression Project to README |
| 9 July | Adding My Credit Card Customer Segmentation Project to README |
| 10 July | Adding My Network Intrusion Detection with Random Forest & XGBoost |
| 10 July | Fixin Project Name |

## Link to other repositories i have
- [My Student Pass/Fail ML Project](https://github.com/BadalovSanan/My-StudentPassFail-ML-Project)
- [Concrete Strength Linear Regression](https://github.com/BadalovSanan/concrete-strength-linear-regression)
- [Credit Card Customer Segmentation](https://github.com/BadalovSanan/credit-card-customer-segmentation)
- [Network Intrusion Detection with Random Forest & XGBoost](https://github.com/BadalovSanan/Network-Intrusion-Detection-with-Random-Forest-and-XGBoost)
