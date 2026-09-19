# Experiment 5: Resampling Methods - Bootstrap & Permutation Testing

## 📌 Experiment Overview
**Experiment 5** explores computer-intensive **Resampling Methods** in statistics:
1. **Non-parametric Bootstrap Resampling** (1,000 iterations) to estimate the sampling distribution of mean glucose and calculate empirical 95% percentile confidence intervals.
2. **Permutation Hypothesis Testing** (1,000 shuffles) to evaluate whether the observed difference in mean glucose between diabetic and non-diabetic patients is statistically significant without making strong parametric distribution assumptions.

---

## 📑 Dataset & Variables

- **Dataset Name**: Pima Indians Diabetes Dataset (`diabetes.csv`)
- **Dataset Location**: Root directory (`../diabetes.csv`)
- **Analyzed Variable**: `Glucose` concentration (mg/dL)
- **Groups**:
  - Non-diabetic (`Outcome == 0`): $N_0 = 500$, Sample Mean $\bar{x}_0 \approx 109.98$ mg/dL
  - Diabetic (`Outcome == 1`): $N_1 = 268$, Sample Mean $\bar{x}_1 \approx 141.26$ mg/dL
  - **Observed Difference ($\Delta \bar{x}$)**: $141.26 - 109.98 = 31.28$ mg/dL

---

## 🛠️ Step-by-Step Instructions to Run the Program

### Prerequisites
Install required Python libraries:
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Execution Steps
1. Navigate to the `Experiment 5` directory:
   ```bash
   cd "Experiment 5"
   ```
2. Launch Jupyter Notebook:
   ```bash
   jupyter notebook exp5.ipynb
   ```
3. Open `exp5.ipynb` and run all cells (`Cell` -> `Run All`).

---

## 📊 Key Findings & Resampling Results

### 1. Bootstrap Resampling Summary (1,000 Replicates)
- **Bootstrap Replicates**: 1,000 bootstrap mean values generated via sampling with replacement ($n=768$).
- **95% Bootstrap Percentile Confidence Interval**:
  - **Lower Limit ($2.5^{th}$ percentile)**: $\approx 118.66$ mg/dL
  - **Upper Limit ($97.5^{th}$ percentile)**: $\approx 123.16$ mg/dL

---

### 2. Permutation Test Summary (1,000 Shuffles)

| Metric / Parameter | Value / Finding | Notes |
| :--- | :--- | :--- |
| **Observed Mean Difference** | $31.28$ mg/dL | $\bar{x}_{\text{diabetic}} - \bar{x}_{\text{non-diabetic}}$ |
| **Number of Permutations** | 1,000 | Group labels randomly shuffled |
| **Permutation Distribution Mean** | $\approx 0.00$ mg/dL | Centered around 0 under Null Hypothesis |
| **Empirical P-Value** | $0.000$ | Proportion of permutation diffs $\ge$ observed diff |
| **Significance Level ($\alpha$)** | 0.05 | Benchmark for hypothesis decision |
| **Final Decision** | **Reject Null Hypothesis ($H_0$)** | Glucose levels are significantly higher in diabetic patients |

---

## 🖼️ Output Screenshots

> [!NOTE]
> Below are placeholders for resampling distribution plots generated in `exp5.ipynb`.

### 1. Bootstrap Distribution of Mean Glucose
*Histogram with KDE curve and 95% Confidence Interval limit lines.*

![Bootstrap Distribution](images/bootstrap_distribution.png)
*(Placeholder: Run Cell [6] in exp5.ipynb)*

---

### 2. Permutation Distribution & Observed Difference
*Permutation null distribution centered at 0 with vertical line showing the observed mean difference (31.28).*

![Permutation Distribution](images/permutation_distribution.png)
*(Placeholder: Run Cell [12] in exp5.ipynb)*

---

### 3. Hypothesis Decision Output
*Console output confirming rejection of the null hypothesis ($p < 0.05$).*

![Hypothesis Decision](images/hypothesis_decision_output.png)
*(Placeholder: Run Cell [13] in exp5.ipynb)*

---

## 📝 How to Add Content & Output Screenshots to this README

Follow these steps to update resampling plots and screenshots:

1. **Create Image Folder**:
   ```bash
   mkdir images
   ```
2. **Export Visual Plots from Code**:
   Add Python save commands before `plt.show()` in `exp5.ipynb`:
   ```python
   plt.savefig("images/bootstrap_distribution.png", bbox_inches='tight', dpi=300)
   plt.savefig("images/permutation_distribution.png", bbox_inches='tight', dpi=300)
   ```
3. **Embed in Markdown**:
   Update markdown image tags:
   ```markdown
   ![Bootstrap Distribution](images/bootstrap_distribution.png)
   ![Permutation Distribution](images/permutation_distribution.png)
   ```
4. **Update Resampling Results**:
   Update bootstrap percentile confidence interval values or empirical p-values in the markdown summary tables above.
