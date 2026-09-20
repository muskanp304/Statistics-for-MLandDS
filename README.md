# Statistics for Machine Learning & Data Science (Stats AIDS)

Welcome to the **Statistics for Machine Learning & Data Science** repository! This repository contains a structured collection of practical experiments focused on exploratory data analysis (EDA), descriptive statistics, data preprocessing, distance metrics, feature scaling, statistical inference, hypothesis testing, and resampling methods (bootstrap & permutation testing).

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
│   ├── README.md                   # Detailed Guide for Exp 1
│   └── images/                     # Output figures (Outcome dist, Histograms, Heatmap, Scatter)
│
├── Experiment 2/                   # Experiment 2: Descriptive Statistics & Data Visualization
│   ├── Exp2.ipynb                  # Jupyter Notebook for Experiment 2
│   ├── README.md                   # Detailed Guide for Exp 2
│   └── images/                     # Output figures (Summary Table, Boxplots, Histograms)
│
├── Experiment 3/                   # Experiment 3: Data Preprocessing, Imputation & Scaling
│   ├── exp3.ipynb                  # Jupyter Notebook for Experiment 3
│   ├── README.md                   # Detailed Guide for Exp 3
│   └── images/                     # Output figures (Imputed Heatmap, Distance Metrics, Scaling)
│
├── Experiment 4/                   # Experiment 4: Statistical Inference & Hypothesis Testing
│   ├── exp4.ipynb                  # Jupyter Notebook for Experiment 4
│   ├── README.md                   # Detailed Guide for Exp 4
│   └── images/                     # Output figures (Confidence Intervals, t-Test, Chi-Square)
│
└── Experiment 5/                   # Experiment 5: Resampling Methods (Bootstrap & Permutation)
    ├── exp5.ipynb                  # Jupyter Notebook for Experiment 5
    ├── README.md                   # Detailed Guide for Exp 5
    └── images/                     # Output figures (Bootstrap & Permutation Distributions)
```

---

## 📊 Overview of Experiments

| Directory | Topic | Key Concepts / Techniques | Primary Dataset | Visual Highlights |
| :--- | :--- | :--- | :--- | :--- |
| [**Experiment 1**](./Experiment%201/README.md) | Exploratory Data Analysis (EDA) | Data summary, Zero values inspection, IQR Outlier Detection, Boxplots, Heatmap | `diabetes.csv` | ![Exp 1 Preview](./Experiment%201/images/correlation_heatmap.png) |
| [**Experiment 2**](./Experiment%202/README.md) | Descriptive Statistics & Visualization | Central Tendency (Mean, Median, Mode), Dispersion (Var, Std, Min, Max), Skewness | `diabetes.csv` | ![Exp 2 Preview](./Experiment%202/images/descriptive_summary_table.png) |
| [**Experiment 3**](./Experiment%203/README.md) | Data Preprocessing & Scaling | Median Imputation, Distance Metrics (Euclidean, Manhattan, Cosine), `StandardScaler` | `diabetes.csv` | ![Exp 3 Preview](./Experiment%203/images/standardization_comparison.png) |
| [**Experiment 4**](./Experiment%204/README.md) | Statistical Inference & Testing | Point Estimates, 95% Confidence Intervals, One-sample t-test, Two-sample t-test, Chi-Square | `diabetes.csv` | ![Exp 4 Preview](./Experiment%204/images/two_sample_ttest_output.png) |
| [**Experiment 5**](./Experiment%205/README.md) | Resampling Methods | Non-parametric Bootstrap Confidence Intervals, Permutation Hypothesis Testing | `diabetes.csv` | ![Exp 5 Preview](./Experiment%205/images/bootstrap_distribution.png) |

---

## 🖼️ Visual Gallery of Key Experiment Outputs

<details>
<summary><b>Click to expand Visual Gallery</b></summary>

### Experiment 1: Correlation Matrix Heatmap
![Correlation Heatmap](./Experiment%201/images/correlation_heatmap.png)

### Experiment 2: Descriptive Statistics Summary Table
![Descriptive Statistics](./Experiment%202/images/descriptive_summary_table.png)

### Experiment 3: Feature Standardization (Before vs. After)
![Standardization Comparison](./Experiment%203/images/standardization_comparison.png)

### Experiment 4: Independent Two-Sample t-Test Results
![t-Test Output](./Experiment%204/images/two_sample_ttest_output.png)

### Experiment 5: Non-Parametric Bootstrap Distribution
![Bootstrap Distribution](./Experiment%205/images/bootstrap_distribution.png)

</details>

---

## 💾 Datasets Used

### Pima Indians Diabetes Dataset (`diabetes.csv`)
- **Rows**: 768 | **Columns**: 9
- **Description**: Medical diagnostic measurements for female patients of Pima Indian heritage aged 21 and older.
- **Target Variable**: `Outcome` (0 = Non-diabetic, 1 = Diabetic)
- **Features**: `Pregnancies`, `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`, `DiabetesPedigreeFunction`, `Age`.

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
Navigate to any experiment directory (e.g., `Experiment 1/`) and open the notebook file (`Exp1.ipynb`).

---

## 📝 How to Update & Maintain Documentation

Every experiment folder contains its own `README.md` documenting specific datasets, methodology, execution steps, output summaries, output screenshots, and step-by-step editing instructions.

To update or add new content to any experiment's `README.md`:
1. **Navigate to the target folder**: e.g., `Experiment 1/`.
2. **Open `README.md`**: Follow the uniform template structure present in each folder.
3. **Add Output Screenshots**:
   - Save output plots into the `images/` subfolder inside that experiment folder.
   - Reference them in Markdown format: `![Description](images/your_screenshot.png)`.
4. **Update Results**: Document key metrics, p-values, or observations directly in the summary table section.

---

## 📜 License & Acknowledgments
This repository is created for learning statistical concepts in Machine Learning & Data Science.
