# **Data Cleaning and Preprocessing Task - Customer Personality Analysis**

## **Task Overview**
This task focuses on performing **data cleaning and preprocessing** on the **Customer Personality Analysis Dataset**. The dataset contains customer information that requires cleaning, handling missing values, standardizing certain columns, and transforming data types for further analysis.

## **Dataset**
The dataset `marketing_campaign.csv` includes customer demographic and behavioral data. It has columns like `Education`, `Marital_Status`, `Income`, and `dt_customer`, which contain various inconsistencies and missing values.

### **Key Columns:**
- `Education`: Customer's education level.
- `Marital_Status`: Customer's marital status.
- `Income`: Customer's income.
- `dt_customer`: The date when the customer joined.

## **Data Preprocessing Steps**
### 1. **Handling Missing Values**
   - **Income**: The missing values in the `Income` column were replaced using **median imputation** to avoid bias.

### 2. **Removing Duplicates**
   - Checked for and identified duplicate rows in the dataset.

### 3. **Standardizing Categorical Columns**
   - The values in `Education` and `Marital_Status` were standardized to remove inconsistencies:
     - `Education`: 
       - '2n Cycle' → 'Master'
       - 'Graduation' → 'Graduate'
     - `Marital_Status`: 
       - 'Together' → 'Married'
       - 'Alone' → 'Single'
       - 'Widow' → 'Widowed'
       - 'Absurd' → 'Other'
       - 'YOLO' → 'Other'

### 4. **Renaming Columns**
   - Columns were renamed to a consistent format (lowercase, underscores replacing spaces, and removal of special characters).

### 5. **Converting Date Format**
   - The `dt_customer` column, initially in object format, was converted to **datetime** to facilitate time-based analysis.

### 6. **Final Output**
   - The cleaned and preprocessed dataset was saved as `marketing_campaign_preprocessed.csv` for potential future use in analysis or modeling.

## **How to Use the Cleaned Data**

To use the preprocessed dataset:

```python
import pandas as pd

# Load the preprocessed dataset
df = pd.read_csv('marketing_campaign_preprocessed.csv')

# Display the first few rows
df.head()
```
## **File Structure**

- `marketing_campaign.csv`: Raw dataset before cleaning.

- `marketing_campaign_preprocessed.csv`: Cleaned and preprocessed dataset.

## **Dependencies**

This task uses the following Python library:

- `pandas`: For data manipulation and preprocessing.

To install `pandas`:
```pip install pandas```


