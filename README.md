# Statistics for Machine Learning & Data Science (Stats AIDS)

Welcome to the **Statistics for Machine Learning & Data Science** repository! This repository contains a structured collection of practical experiments and assignments focused on exploratory data analysis, descriptive statistics, data preprocessing, distance metrics, feature scaling, statistical inference, hypothesis testing, resampling methods, and predictive regression modeling.

---

## 📂 Repository Structure

```directory
Statistics-for-MLandDS/
│
├── diabetes.csv                    # Pima Indians Diabetes Dataset
├── README.md                       # Main Repository Documentation (This file)
│
├── Experiment 1/                   # Experiment 1: EDA & Data Quality Assessment
│   ├── Exp1.ipynb                  # Jupyter Notebook for Experiment 1
│   └── README.md                   # Detailed Documentation & Guide for Exp 1
│
├── Experiment 2/                   # Experiment 2: Descriptive Statistics & Data Visualization
│   ├── Exp2.ipynb                  # Jupyter Notebook for Experiment 2
│   └── README.md                   # Detailed Documentation & Guide for Exp 2
│
├── Experiment 3/                   # Experiment 3: Data Preprocessing, Imputation & Scaling
│   ├── exp3.ipynb                  # Jupyter Notebook for Experiment 3
│   └── README.md                   # Detailed Documentation & Guide for Exp 3
│
├── Experiment 4/                   # Experiment 4: Statistical Inference & Hypothesis Testing
│   ├── exp4.ipynb                  # Jupyter Notebook for Experiment 4
│   └── README.md                   # Detailed Documentation & Guide for Exp 4
│
├── Experiment 5/                   # Experiment 5: Resampling Methods (Bootstrap & Permutation)
│   ├── exp5.ipynb                  # Jupyter Notebook for Experiment 5
│   └── README.md                   # Detailed Documentation & Guide for Exp 5
│
└── Assignment3/                    # Assignment 3: California Housing Regression Analysis
    ├── Eda.ipynb                   # Jupyter Notebook for California Housing Analysis
    ├── housing.csv                 # California Housing Dataset
    └── README.md                   # Detailed Documentation & Guide for Assignment 3
```

---

## 📊 Overview of Experiments

| Directory | Topic | Key Concepts / Techniques | Primary Dataset |
| :--- | :--- | :--- | :--- |
| [**Experiment 1**](./Experiment%201/README.md) | Exploratory Data Analysis (EDA) | Data summary, Data types, Zero values, IQR Outlier Detection, Boxplots, Correlation Heatmap, Pairplots | `diabetes.csv` |
| [**Experiment 2**](./Experiment%202/README.md) | Descriptive Statistics & Visualization | Central Tendency (Mean, Median, Mode), Dispersion (Var, Std, Min, Max), Skewness, Visual Plots | `diabetes.csv` |
| [**Experiment 3**](./Experiment%203/README.md) | Data Preprocessing & Distance Metrics | Median Imputation, Correlation Matrix, Distance Metrics (Euclidean, Manhattan, Cosine), `StandardScaler` | `diabetes.csv` |
| [**Experiment 4**](./Experiment%204/README.md) | Statistical Inference & Hypothesis Testing | Point Estimates, 95% Confidence Intervals, One-sample t-test, Two-sample t-test, Chi-Square Test | `diabetes.csv` |
| [**Experiment 5**](./Experiment%205/README.md) | Resampling Methods | Non-parametric Bootstrap Confidence Intervals, Permutation Hypothesis Testing, Empirical p-values | `diabetes.csv` |
| [**Assignment 3**](./Assignment3/README.md) | Regression Analysis & Evaluation | EDA, Median Imputation, One-Hot Encoding, Linear / Ridge / Lasso / ElasticNet Regression, MAE/MSE/RMSE/R² | `housing.csv` |

---

## 💾 Datasets Used

### 1. Pima Indians Diabetes Dataset (`diabetes.csv`)
- **Rows**: 768 | **Columns**: 9
- **Description**: Medical diagnostic measurements for female patients of Pima Indian heritage aged 21 and older.
- **Target Variable**: `Outcome` (0 = Non-diabetic, 1 = Diabetic)
- **Features**: `Pregnancies`, `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`, `DiabetesPedigreeFunction`, `Age`.

### 2. California Housing Dataset (`housing.csv` in `Assignment3/`)
- **Rows**: 20,640 | **Columns**: 10
- **Description**: Metrics derived from the 1990 California census for housing block groups.
- **Target Variable**: `median_house_value`
- **Features**: `longitude`, `latitude`, `housing_median_age`, `total_rooms`, `total_bedrooms`, `population`, `households`, `median_income`, `ocean_proximity`.

---

## 🚀 Setup & Execution Instructions

### Prerequisites
Ensure you have **Python 3.8+** installed along with Jupyter Notebook or VS Code with Jupyter extension.

### Step 1: Clone the Repository
```bash
git clone https://github.com/muskanp304/Statistics-for-MLandDS.git
cd Statistics-for-MLandDS
```

### Step 2: Create & Activate Virtual Environment (Optional but Recommended)
- **Windows (PowerShell)**:
  ```powershell
  python -m venv venv
  .\venv\Scripts\Activate.ps1
  ```
- **Linux / macOS**:
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

### Step 3: Install Required Dependencies
```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
```

### Step 4: Launch Jupyter Notebook
```bash
jupyter notebook
```
Navigate to any experiment directory (e.g., `Experiment 1/`) and open the notebook file (`.ipynb`).

---

## 📝 How to Update & Maintain READMEs in Each Experiment Folder

Every experiment folder contains its own `README.md` documenting specific datasets, methodology, execution steps, output summaries, output screenshots, and step-by-step editing instructions.

To update or add new content to any experiment's `README.md`:
1. **Navigate to the target folder**: e.g., `Experiment 1/`.
2. **Open `README.md`**: Follow the uniform template structure present in each folder.
3. **Add Output Screenshots**:
   - Save your output plots/screenshots into an `images/` or `assets/` subfolder inside that experiment folder.
   - Reference them in Markdown format: `![Description](images/your_screenshot.png)`.
4. **Update Results**: Document key metrics, p-values, or observations directly in the summary table section.

---

## 📜 License & Acknowledgments
This repository is created for learning statistical concepts in Machine Learning & Data Science.
