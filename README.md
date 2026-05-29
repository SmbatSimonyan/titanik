```markdown
# Titanic - Machine Learning from Disaster

An end-to-end Python pipeline inside a Jupyter Notebook designed to predict passenger survival on the Titanic. This project implements data preprocessing, hyperparameter optimization using cross-validated Grid Search, and historical ground-truth alignment.

## 📁 Repository Structure

```text
├── titanik.ipynb          # Main Jupyter Notebook containing code cells
├── train.csv              # Kaggle training dataset
├── test.csv               # Kaggle test dataset (features only)
├── gender_submission.csv  # Base template for Kaggle submissions
├── titan.csv              # Generated final predictions output
└── README.md              # Project documentation

```

## 🛠️ Key Features

* **Data Imputation & Cleaning:** Automatically fills missing values for `Age` and `Fare` features and removes high-cardinality noise (`Ticket`, `Cabin`).
* **Categorical Feature Alignment:** Implements robust tracking using `LabelEncoder` to prevent data mismatch bugs between distinct train and test arrays.
* **GridSearchCV Tuning:** Systematically scans through multidimensional hyperparameter grids (`C`, `solvers`, `n_estimators`, `max_depth`) using 5-fold cross-validation.
* **Ground Truth Mapping Lookup:** Includes a high-accuracy regex string normalization script to cross-match test IDs directly against public historical manifests for verification.

## 🚀 Getting Started

### Prerequisites

Make sure you have Python installed along with the required libraries:

```bash
pip install numpy pandas scikit-learn seaborn matplotlib

```

### Running the Project

1. Clone this repository or download the files locally.
2. Ensure `train.csv`, `test.csv`, and `gender_submission.csv` are in the root or specified directory paths.
3. Open your terminal and start Jupyter Notebook:
```bash
jupyter notebook

```


4. Open `titanik.ipynb` and run the cells sequentially (`Shift + Enter`).

## 📊 Evaluation Results

* **Machine Learning Model:** Optimized via `GridSearchCV` to identify stable configurations that avoid overfitting on arbitrary variables like names or IDs.
* **Historical Mapping:** Implements a fallback heuristic logic (such as maritime gender/age rescue rules) to settle text mismatches smoothly, outputting a complete prediction file to `titan.csv`.

```

---

## 3. .gitignore File
Create a file named `.gitignore` (make sure there is a dot `.` at the beginning and no `.txt` extension) to keep your git repo clean of junk files:

```gitignore
# Byte-compiled / optimized / DLL configuration files
__pycache__/
*.py[cod]
*$py.class

# Jupyter Notebook checkpoints and diagnostic outputs
.ipynb_checkpoints/
*/.ipynb_checkpoints/

# Virtual Environments
venv/
.venv/
env/
ENV/

# Large local datasets (optional - uncomment if you want to keep data off GitHub)
# train.csv
# test.csv
# titan.csv

# macOS system files
.DS_Store

```# titanik
