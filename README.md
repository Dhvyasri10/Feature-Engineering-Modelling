# Feature-Engineering-Modelling
#PowerCo Churn Analysis – Feature Engineering
##📊 Project Overview
This project focuses on feature engineering for churn prediction at PowerCo, a gas and electricity utility company. The goal is to create new features, optimize existing ones, and transform the data to improve the performance of predictive models. This is part of a broader initiative to diagnose and prevent customer churn by identifying key influencing factors.
---
##📁 **Dataset Description**
The project uses three datasets provided by PowerCo:

1. **Historical Customer Data:**

-Contains customer details such as usage, sign-up date, and forecasted consumption.
Helps in identifying customer behavior and patterns.
Historical Pricing Data:

-Includes variable and fixed pricing information across different periods.
Captures fluctuations in pricing over time.
2. **Churn Indicator Data:**

Specifies whether a customer has churned or not.
Acts as the target variable for churn prediction modeling.
--
##⚙️ **Tech Stack and Libraries**
- **Language:** Python
- **Libraries:**
- 'pandas': for data manipulation
- 'numpy': for numerical operations
- 'matplotlib': for visualizations
- 'seaborn': for statistical plots
- 'plotly': for interactive visualizations
- 'scipy': for statistical transformations
- 'sklearn': for encoding and transformations
- **Jupyter Notebook**: for interactive analysis and visualizations
---
##🔥 **Feature Engineering Steps**
###✅ **1. Data Preprocessing**
- Column Removal:
- Identified and removed irrelevant or redundant columns (e.g., columns with only one unique value).
- Missing Value Treatment:
- Handled missing values using imputation techniques or removal when necessary.
- Data Type Conversion:
- Ensured consistent data types (e.g., converting date columns to datetime format) for accurate analysis.
###🔥 2. **New Feature Creation**
- Date Transformation:
- Extracted year, month, and day from date columns for better temporal analysis.
- Removed the original date columns after extraction to reduce redundancy.
- Period-based Price Changes:
- Created features for average and maximum price changes across different periods (peak, mid-peak, and off-peak).
- These features represent the price variance that could influence customer churn.
- Price Difference Across Months:
- Calculated the monthly price difference to capture seasonal price fluctuations.
- Helps in detecting price-sensitive churn patterns.
##🔥 3.** Feature Combination**
- Column Merging:
- Combined related columns to create aggregate features (e.g., total usage, combined pricing metrics).
- Dataset Merging:
- Merged datasets using common columns (Customer ID or unique keys) for a unified dataset.
- Ensured data integrity by validating the merge operations.
##🔥 4. **Feature Transformation**
- Boolean to Binary Conversion:
- Converted boolean columns into 0 and 1 values to prepare for modeling.
- Categorical to Dummy Variables:
- Applied One-Hot Encoding to convert categorical columns into dummy variables.
- Skewness Treatment:
- Applied logarithmic transformation to skewed columns for a more normal distribution.
- Improved model performance by reducing the impact of skewed data.
##🔥 5. **Correlation Analysis**
- Correlation Matrix:
- Visualized correlations between features using a heatmap.
- Identified and removed highly correlated columns to prevent multicollinearity.
- Feature Selection:
- Removed redundant or irrelevant features, ensuring only the most informative features are retained for modeling.
---
##📈 **Key Findings**
- Price Variation Impact:
- Customers with higher price variance across periods are more likely to churn.
- Suggests that fluctuating pricing strategies impact customer retention.
- Monthly Price Changes:
- Significant monthly price fluctuations correlate with higher churn rates.
- Indicates that inconsistent pricing may drive customer dissatisfaction.
**Feature Importance:**
- Newly created features (e.g., price changes, date transformations) show higher importance scores during model training, indicating their effectiveness in churn prediction.
