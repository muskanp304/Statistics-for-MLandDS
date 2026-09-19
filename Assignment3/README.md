# Assignment 3: California Housing Price Prediction & Regression Modeling

## 📌 Assignment Overview
**Assignment 3** covers an end-to-end Machine Learning regression workflow using the **California Housing Dataset**. The notebook (`Eda.ipynb`) performs exploratory data analysis, handles missing data via median imputation, encodes categorical variables using one-hot encoding, standardizes numerical features, trains four different regression models (Linear Regression, Ridge, Lasso, and ElasticNet), and evaluates their predictive performance using MAE, MSE, RMSE, and $R^2$ score.

---

## 📑 Dataset Details

- **Dataset Name**: California Housing Dataset (`housing.csv`)
- **Dataset Location**: `Assignment3/housing.csv`
- **Total Records (Rows)**: 20,640
- **Total Columns**: 10 (9 predictor variables + 1 continuous target variable)

### Feature Attribute Summary

| Feature Name | Data Type | Description | Handling / Preprocessing |
| :--- | :--- | :--- | :--- |
| **longitude** | Numerical (float64) | Longitude measure for block | Standard Scaled |
| **latitude** | Numerical (float64) | Latitude measure for block | Standard Scaled |
| **housing_median_age** | Numerical (float64) | Median age of a house within a block | Standard Scaled |
| **total_rooms** | Numerical (float64) | Total number of rooms within a block | Standard Scaled |
| **total_bedrooms** | Numerical (float64) | Total number of bedrooms within a block | Imputed (207 missing values replaced with median) & Scaled |
| **population** | Numerical (float64) | Total number of people residing within a block | Standard Scaled |
| **households** | Numerical (float64) | Total number of households within a block | Standard Scaled |
| **median_income** | Numerical (float64) | Median income for households within a block (in tens of thousands USD) | Standard Scaled |
| **ocean_proximity** | Categorical (object) | Location of house relative to ocean (`<1H OCEAN`, `INLAND`, `NEAR OCEAN`, `NEAR BAY`, `ISLAND`) | One-Hot Encoded (`pd.get_dummies(..., drop_first=True)`) |
| **median_house_value** | Numerical (float64) | **Target Variable**: Median house value for households within a block (in USD) | Output variable ($y$) |

---

## 🛠️ Step-by-Step Instructions to Run the Program

### Prerequisites
Install required Python libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Execution Steps
1. Navigate to the `Assignment3` directory:
   ```bash
   cd Assignment3
   ```
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook Eda.ipynb
   ```
3. Open `Eda.ipynb` and execute all cells sequentially (`Cell` -> `Run All`).

---

## 📊 Model Evaluation & Results Summary

### Train-Test Configuration
- **Train-Test Split Ratio**: 80% Training Data ($N = 16,512$), 20% Testing Data ($N = 4,128$)
- **Random State**: 42

### Model Comparison Table (Extracted from Notebook Cell [15])

| Model | MAE | MSE | RMSE | R² Score |
| :--- | :---: | :---: | :---: | :---: |
| **Linear Regression** | ~50,523.58 | ~4.83 $\times 10^9$ | ~69,500.28 | ~0.6488 |
| **Ridge Regression** ($\alpha=1.0$) | ~50,526.47 | ~4.83 $\times 10^9$ | ~69,501.95 | ~0.6488 |
| **Lasso Regression** ($\alpha=0.1$) | ~50,523.63 | ~4.83 $\times 10^9$ | ~69,500.30 | ~0.6488 |
| **Elastic Net** ($\alpha=0.1, l_1\text{-ratio}=0.5$) | ~51,912.44 | ~5.10 $\times 10^9$ | ~71,438.30 | ~0.6289 |

---

## 🖼️ Output Screenshots

> [!NOTE]
> Below are placeholders for figures and table outputs generated in `Eda.ipynb`.

### 1. Data Cleaning & Null Value Check Printout
*Output showing missing value counts before and after median imputation.*

![Data Cleaning Output](images/data_cleaning_output.png)
*(Placeholder: Run Cells [4] & [6] in Eda.ipynb)*

---

### 2. Model Performance Evaluation Table
*Comparison DataFrame display showing MAE, MSE, RMSE, and R² score across all 4 regression models.*

![Model Evaluation Table](images/model_evaluation_table.png)
*(Placeholder: Run Cell [15] in Eda.ipynb)*

---

## 📝 How to Add Content & Output Screenshots to this README

Follow these steps to update or add your output images and documentation:

1. **Create Image Directory**:
   ```bash
   mkdir images
   ```
2. **Save Figures & Screenshots**:
   Save cell outputs as PNG files inside `Assignment3/images/`.
3. **Embed Screenshots**:
   Update markdown image references:
   ```markdown
   ![Model Evaluation Table](images/model_evaluation_table.png)
   ```
4. **Update Results Table**:
   Update evaluation metrics in the comparison Markdown table above when hyperparameter tuning or feature engineering is modified.
