# 📊 Student Exam Score Prediction

A machine learning project that predicts student exam scores based on lifestyle, study habits, and academic factors using **Linear Regression**, **Random Forest**, and **XGBoost** models.

---

## 📁 Project Structure

```
├── linear_regression.ipynb   # Main notebook with EDA, preprocessing & modeling
├── .gitignore                # Excludes dataset files
└── README.md
```
> ⚠️ `train.csv` is **not included** in this repo due to file size. See the **Dataset** section below to download it.

---

## 📌 Problem Statement

Predict a student's `exam_score` given various features such as sleep quality, study method, internet access, course difficulty, and more.

---

## 🗂️ Dataset Features

| Feature | Type | Description |
|---|---|---|
| `sleep_quality` | Categorical | poor / average / good |
| `facility_rating` | Categorical | low / medium / high |
| `exam_difficulty` | Categorical | easy / moderate / hard |
| `internet_access` | Binary | yes / no |
| `gender` | Categorical | One-hot encoded |
| `study_method` | Categorical | One-hot encoded |
| `course` | Categorical | One-hot encoded |
| `exam_score` | Numerical | **Target variable** |

---

## ⚙️ Workflow

### 1. Exploratory Data Analysis (EDA)
- Checked for null values, data types, unique values
- Descriptive statistics with `df.describe()`

### 2. Data Preprocessing
- Ordinal encoding for `sleep_quality`, `facility_rating`, `exam_difficulty`
- Binary encoding for `internet_access`
- One-hot encoding (with `drop_first=True`) for `gender`, `study_method`, `course`
- Converted boolean columns to integers

### 3. Model Training
Data split: **80% train / 20% test** (`random_state=42`)

| Model | Key Parameters |
|---|---|
| Linear Regression | Default (sklearn) |
| Random Forest | 500 trees, max_depth=20, min_samples_split=5 |
| XGBoost | 500 estimators, lr=0.05, max_depth=6, subsample=0.8 |

### 4. Evaluation Metrics
- **R² Score** — measures how well the model explains variance
- **RMSE** — Root Mean Squared Error

---

## 🛠️ Tech Stack

- Python 3.x
- [NumPy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/) & [Seaborn](https://seaborn.pydata.org/)
- [Scikit-learn](https://scikit-learn.org/)
- [XGBoost](https://xgboost.readthedocs.io/)

---

## 📥 Dataset

The dataset is **not included** in this repository due to its size.

1. Download it from Kaggle: [🔗 Playground Series S6E1 - train.csv](https://www.kaggle.com/competitions/playground-series-s6e1/data?select=train.csv)
2. Place `train.csv` in the root folder of the project before running the notebook.

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install dependencies
```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost
```

### 3. Run the notebook
```bash
jupyter notebook linear_regression.ipynb
```

> ⚠️ Make sure `train.csv` is in the same directory, or update the file path inside the notebook.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
