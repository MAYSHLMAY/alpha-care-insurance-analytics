# AlphaCare Insurance Analytics

## Project Overview

**AlphaCare Insurance Solutions (ACIS)** aims to optimize its car insurance offerings in South Africa by identifying low-risk customer segments and building predictive models for risk-based premium optimization. This project involves **End-to-End Insurance Risk Analytics & Predictive Modeling**, covering:

- Exploratory Data Analysis (EDA)  
- Statistical Hypothesis Testing (A/B Testing)  
- Predictive Modeling (Linear Regression, Random Forest, XGBoost)  
- Feature Importance and Model Interpretability (SHAP/LIME)  
- Data Version Control (DVC) for reproducibility  

This repository contains **notebooks, scripts, and DVC-tracked datasets** to support analysis and modeling.

---

## Business Objective

The main goal is to help ACIS:

1. Identify “low-risk” customers where premiums can be optimized.  
2. Understand risk drivers across geography, vehicle type, gender, and policy features.  
3. Build predictive models to estimate claim severity and optimal premium.  
4. Provide actionable recommendations to optimize marketing strategy and product offerings.

---

## Repository Structure

```

alpha-care-insurance-analytics/
│
├─ data/                       # Raw and processed data tracked via DVC
│  ├─ MachineLearningRating_v3.txt
│  └─ MachineLearningRating_v3_csv.csv
│
├─ notebooks/                  # Task-specific notebooks
│  ├─ insurance_eda_task1.ipynb
│  ├─ hypothesis_testing_task3.ipynb
│  ├─ statistical_modeling_task4.ipynb
│  └─ README.md
│
├─ scripts/                    # Python scripts for analysis
│  ├─ hypothesis_test.py
│  ├─ statistical_modeling.py
│  ├─ utils.py
│  └─ **init**.py
│
├─ src/                        # Python modules (optional)
│  └─ **init**.py
│
├─ tests/                      # Unit tests (optional)
│  └─ **init**.py
│
├─ .gitignore                  # Git ignore file
├─ .dvcignore                  # DVC ignore file
├─ README.md
├─ requirements.txt
└─ MachineLearningRating_v3.txt.dvc  # DVC tracked dataset

````

> ⚠️ Ignored files: `.git/`, `.dvc/cache/`, `__pycache__/`, notebook checkpoints, virtual environments.

---

## Tasks and Workflow

The project was divided into **4 main tasks**, each handled in separate Git branches:

### **Task 1 — Exploratory Data Analysis (EDA)**
- **Branch:** `task-1`  
- **Files:** `notebooks/insurance_eda_task1.ipynb`  
- Activities:
  - Data understanding and structure assessment  
  - Descriptive statistics and univariate/multivariate analysis  
  - Visualization of TotalPremium, TotalClaims, and risk factors  

### **Task 2 — Data Version Control (DVC)**
- **Branch:** `task-2`  
- **Files:** `MachineLearningRating_v3.txt.dvc`, `.dvcignore`  
- Activities:
  - DVC initialization and setup of local remote storage  
  - Version control for datasets for reproducibility  
  - Push dataset to local remote  

### **Task 3 — Hypothesis Testing (A/B Testing)**
- **Branch:** `task-3`  
- **Files:** `notebooks/hypothesis_testing_task3.ipynb`, `scripts/hypothesis_test.py`  
- Activities:
  - KPI selection and data segmentation  
  - Statistical tests across provinces, zip codes, and gender  
  - Documentation and interpretation of results for business recommendations  

### **Task 4 — Predictive Modeling**
- **Branch:** `task-4`  
- **Files:** `notebooks/statistical_modeling_task4.ipynb`, `scripts/statistical_modeling.py`, `scripts/utils.py`, `src/`, `tests/`  
- Activities:
  - Data preprocessing and feature engineering  
  - Model building: Linear Regression, Random Forest, XGBoost  
  - Model evaluation using RMSE, R-squared, and comparison  
  - Feature importance analysis with SHAP/LIME and business interpretation  

---

## Setup & Installation

1. **Clone the repository**

```bash
git clone https://github.com/MAYSHLMAY/alpha-care-insurance-analytics.git
cd alpha-care-insurance-analytics
````

2. **Create and activate Python environment**

```bash
python -m venv venv
# Linux/Mac
source venv/bin/activate
# Windows
venv\Scripts\activate
```

3. **Install requirements**

```bash
pip install -r requirements.txt
```

4. **DVC Setup**

```bash
# Initialize DVC (if not done)
dvc init

# Pull dataset from DVC remote
dvc pull
```

---

## Usage

### Run EDA

```bash
jupyter notebook notebooks/insurance_eda_task1.ipynb
```

### Run Hypothesis Testing

```bash
python scripts/hypothesis_test.py
```

### Run Predictive Modeling

```bash
python scripts/statistical_modeling.py
```

---

## Git Workflow

* **Branching strategy:**

  * `main` → final merged results
  * `task-1` → EDA
  * `task-2` → DVC/data versioning
  * `task-3` → Hypothesis testing
  * `task-4` → Predictive modeling

* **Commits:**

  * Granular, task-specific commits
  * Descriptive messages like:

```
feat(task-1): add descriptive statistics and plots
feat(task-3): implement chi-squared and t-tests
feat(task-4): add feature importance analysis
```

* **Merges:** `--no-ff` to preserve history

---

## References

* [Insurance Analytics Overview](https://www.fsrao.ca/media/11501/download)
* [A/B Testing Guide](https://www.engagys.com/insights/a-b-testing-the-key-to-effective-healthcare-communications)
* [DVC Documentation](https://dvc.org/doc/user-guide)
* [Random Forest Algorithm](https://builtin.com/data-science/random-forest-algorithm)
* [SHAP Documentation](https://shap.readthedocs.io/en/latest/)


