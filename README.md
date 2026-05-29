# Titanic Survival Prediction 🚢

Machine Learning project based on the famous Titanic dataset from Kaggle.

This project focuses on predicting passenger survival using data analysis, preprocessing, feature engineering, and machine learning models.

## Dataset

The dataset comes from the Kaggle Titanic competition:

* [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic?utm_source=chatgpt.com)

The goal is to predict whether a passenger survived or not based on features like:

* Age
* Gender
* Passenger Class
* Fare
* Family Size
* Embarked Port
* And more...

---

## Project Structure

```bash
titanik/
│
├── train.csv
├── test.csv
├── gender_submission.csv
├── notebook.ipynb
├── submission.csv
└── README.md
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Machine Learning Workflow

### 1. Data Cleaning

* Handling missing values
* Encoding categorical features
* Removing unnecessary columns

### 2. Exploratory Data Analysis (EDA)

* Survival distribution
* Gender analysis
* Passenger class analysis
* Correlation visualization

### 3. Feature Engineering

* Family size creation
* Title extraction from names
* Data normalization

### 4. Model Training

Models tested in this project include:

* Logistic Regression
* Random Forest
* Decision Tree
* Gradient Boosting

### 5. Prediction & Submission

Predictions are generated for the test dataset and exported as:

```python
submission.csv
```

---

## Example Code

```python
y_pred = grid_model.predict(X_test)

submission = pd.DataFrame({
    "PassengerId": test["PassengerId"],
    "Survived": y_pred
})

submission.to_csv("submission.csv", index=False)
```

---

## Results

The model was trained and evaluated using the Kaggle Titanic competition dataset.

Main focus:

* Improving prediction accuracy
* Better feature engineering
* Cleaner preprocessing pipeline

---

## How to Run

Clone the repository:

```bash
git clone https://github.com/SmbatSimonyan/titanik.git
```

Install dependencies:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

Run the notebook or Python script.

---

## Author

GitHub: [SmbatSimonyan GitHub Profile](https://github.com/SmbatSimonyan?utm_source=chatgpt.com)

---

## Repository

* [Titanik Repository](https://github.com/SmbatSimonyan/titanik?utm_source=chatgpt.com)

---

## Future Improvements

* Hyperparameter tuning
* Ensemble models
* Deep learning approach
* Better feature engineering
* Cross-validation optimization

---

## License

This project is for educational and learning purposes.
