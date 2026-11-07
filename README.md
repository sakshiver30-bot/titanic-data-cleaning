# Titanic Dataset: Data Cleaning & Preparation

## Dataset
Titanic - Machine Learning from Disaster (train.csv), from Kaggle.
Source: https://www.kaggle.com/competitions/titanic

## Tools Used
Python (pandas) in Google Colab

## Problems Found
| Issue | Details |
|---|---|
| Missing values in Age | 177 |
| Missing values in Cabin | 687 (about 77%) |
| Missing values in Embarked | 2 |
| Duplicate rows | 0 |
| Duplicate PassengerIds | 0 |
| Incorrect data types | Age stored as decimal; Pclass and Survived stored as numbers but are categories |
| Inconsistent values | Sex and Embarked were already consistent; text was still trimmed and standardized |

## Cleaning Steps
1. Checked for duplicate rows (none found, none removed).
2. Filled missing Age values with the median age.
3. Filled the 2 missing Embarked values with the most common port (S).
4. Dropped the Cabin column because about 77% of its values were missing.
5. Trimmed spaces and standardized text case in Sex, Embarked and Name.
6. Converted Age to integer, and Pclass and Survived to category.

## Result
| | Before | After |
|---|---|---|
| Rows | 891 | 891 |
| Columns | 12 | 11 |
| Missing values | 866 | 0 |

## Files
- `train.csv`: original dataset
- `cleaned_data.csv`: cleaned dataset
- `Titanic_Data_Cleaning.ipynb`: notebook with all code

## Notes
Median was used for Age because it is not affected by extreme values.
