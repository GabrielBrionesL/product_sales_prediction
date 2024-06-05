# Sales Data Classification

This repository contains a project for classifying sales data using a Random Forest classifier. The dataset used in this project is `SalesKaggle3.csv` https://www.kaggle.com/datasets/flenderson/sales-analysis, and the objective is to predict the `SoldFlag` based on various features in the dataset.

## Project Structure

- **Data Preprocessing**: Handling historical data, dropping unused columns, and shuffling.
- **Pipeline Construction**: Building a pipeline that includes preprocessing steps and a Random Forest classifier.
- **Cross-Validation**: Using KFold to ensure robust model evaluation.
- **Class Imbalance Handling**: Using RandomOverSampler to handle class imbalance in the training data.

## Dependencies

- numpy
- pandas
- scikit-learn
- imbalanced-learn

Install the dependencies using:
```bash
pip install numpy pandas scikit-learn imbalanced-learn
```

## Dataset

The dataset `SalesKaggle3.csv` should be placed in the same directory as the code. The dataset is expected to contain the following columns:
- `File_Type`
- `Order`
- `SKU_number`
- `SoldCount`
- `SoldFlag`
- `MarketingType`
- `ReleaseNumber`

## Process Overview

1. **Data Loading**: Load the dataset and inspect its structure.
2. **Data Preprocessing**: Filter historical data, drop unused columns, shuffle the dataset, and split it into features (`X`) and target (`y`).
3. **Building the Pipeline**: Construct a machine learning pipeline that includes one-hot encoding for categorical variables and a Random Forest classifier.
4. **Cross-Validation and Model Training**: Use KFold for cross-validation, handle class imbalance using RandomOverSampler, and train the model.
5. **Evaluation**: Calculate and report the average accuracy and F1 score from the cross-validation.

## Results

- **Accuracy**: 76.87%
- **F1-Score**: 0.43494

These results are based on a 5-fold cross-validation process, ensuring the model's robustness and reliability.
