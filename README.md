# 🏠 House Price Predictor

A full end-to-end machine learning project that predicts house prices using the Ames Housing dataset. Built with a blended ensemble of Ridge Regression, XGBoost, and LightGBM — deployed as an interactive Streamlit web app.

**Kaggle Public Score: 0.12540**

---

## 📁 Project Structure

```
house_price_predictor/
├── app.py                  # Streamlit web app
├── data/
│   ├── train.csv           # Training data (from Kaggle)
│   ├── test.csv            # Test data (from Kaggle)
│   ├── X_train.csv         # Preprocessed training features
│   ├── X_test.csv          # Preprocessed test features
│   ├── y_train.csv         # Log-transformed target
│   ├── ridge_model.pkl     # Trained Ridge model
│   ├── xgb_model.pkl       # Trained XGBoost model
│   ├── lgb_model.pkl       # Trained LightGBM model
│   └── submission.csv      # Kaggle submission file
├── notebooks/
│   ├── 01_load_and_inspect.ipynb    # Day 1 - Data loading
│   ├── 02_eda.ipynb                 # Day 2 - Exploratory analysis
│   ├── 03_feature_engineering.ipynb # Day 3 - Feature engineering
│   └── 04_modelling.ipynb           # Day 4 - Model training
├── requirements.txt
└── README.md
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.10 | Core language |
| Pandas & NumPy | Data manipulation |
| Matplotlib & Seaborn | Data visualisation |
| Scikit-learn | ML pipeline & Ridge model |
| XGBoost | Gradient boosting model |
| LightGBM | Gradient boosting model |
| Optuna | Hyperparameter tuning |
| Streamlit | Web app deployment |
| Joblib | Model saving |

---

## 📊 Results

| Model | RMSE |
|---|---|
| Ridge Regression | 0.1154 |
| XGBoost | 0.1170 |
| LightGBM | 0.1178 |
| **Blended Ensemble** | **0.0757** |
| **Kaggle Public Score** | **0.12540** |

---

## ⚙️ How to Run Locally

**1. Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/house-price-predictor.git
cd house-price-predictor
```

**2. Create and activate virtual environment**
```bash
python -m venv venv
venv\Scripts\activate        # Windows
source venv/bin/activate     # Mac/Linux
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Download the dataset from Kaggle**
```bash
kaggle competitions download -c house-prices-advanced-regression-techniques
Expand-Archive house-prices-advanced-regression-techniques.zip -DestinationPath data\
```

**5. Run the notebooks in order**
- `01_load_and_inspect.ipynb`
- `02_eda.ipynb`
- `03_feature_engineering.ipynb`
- `04_modelling.ipynb`

**6. Launch the app**
```bash
streamlit run app.py
```

---

## 🔍 Key Learnings

- **Feature engineering matters more than model choice** — carefully imputing missing values and creating new features like `TotalSF` and `TotalBath` had a bigger impact than switching algorithms
- **Log transforming the target** reduced skewness from 1.88 to 0.12 and significantly improved model performance
- **Blending models beats any single model** — combining Ridge, XGBoost and LightGBM reduced RMSE by 34%
- **Neighborhood is one of the biggest price drivers** — location explained more variance than any other single feature

---

## 📌 Dataset

[Ames Housing Dataset](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) — 79 features describing residential homes in Ames, Iowa.

---

## 👤 Author

**Sujithran Madhiwanan**
- GitHub: [@SujithranM](https://github.com/SujithranM)
- LinkedIn: [Sujithran Madhiwanan](https://linkedin.com/in/sujithran-madhiwanan)
