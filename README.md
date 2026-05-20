# Predicting London House Prices Using Machine Learning

Machine learning framework for predicting historical London residential property prices using structural, geographic, temporal, and historical transaction data.

Built using over 418,000 London property transactions spanning from 1995–2024, this project explores:
- exploratory data analysis (EDA),
- feature engineering,
- ensemble machine learning,
- inflation-adjusted modelling,
- segmented market modelling,
- and SHAP-based model interpretability.

The project was designed to balance predictive accuracy, economic interpretability, and commercial relevance within one of the world’s most heterogeneous real-estate markets.

---

## Key Highlights

- Built machine learning models using over 418,000 London property transactions
- Developed segmented-market Random Forest frameworks for improved predictive accuracy
- Engineered structural, spatial, and temporal housing features
- Investigated inflation-adjusted versus nominal-price modelling
- Applied SHAP analysis for model interpretability
- Evaluated linear, nonlinear, and ensemble learning methods

---

## Final Model Performance

| Market Segment | Final Model | Test RMSE | Test R² |
|---|---|---:|---:|
| Low-price cluster | Random Forest | £79,753 | 0.80 |
| Medium-price cluster | Random Forest | £431,000 | 0.46 |
| High-price cluster | Random Forest | £529,000 | 0.79 |

---

## Main Findings

- Ensemble methods consistently outperformed simpler linear models.
- Segmented market modelling substantially improved predictive performance by reducing market heterogeneity.
- Inflation-adjusted modelling demonstrated that nominal-price models relied heavily on long-term market appreciation trends.
- Geographic variables, floor area, and proximity to Central London emerged as some of the strongest drivers of predicted property prices.
- SHAP analysis showed that different housing-market segments relied on different predictive drivers.

---


## Repository Contents

This repository contains the completed notebooks, final report, and dataset information for the London house price prediction project.

- `EDA.ipynb` — exploratory data analysis, data cleaning, feature investigation, and visualisations.
- `London_House_Price_Prediction_ML_Pipeline.ipynb` — machine learning pipeline, modelling experiments, segmented modelling, and SHAP interpretation.
- `Final_Capstone_Report.pdf` — final written report summarising the full project.
- `README.md` — project overview and key results.
- Data-Inflation.csv

---

## Technologies Used

- Python
- pandas
- NumPy
- scikit-learn
- XGBoost
- LightGBM
- SHAP
- matplotlib
- seaborn
- Jupyter Notebook

---

## Dataset

The dataset used in this project is the Kaggle dataset and inflation.csv:

**London House Price Data** by Jake Wright.

Due to file-size and licensing considerations, the dataset is not included directly within this repository.

E## Dataset

The dataset used in this project was downloaded directly from Kaggle using `kagglehub`.

```python
path = kagglehub.dataset_download("jakewright/house-price-data")

csv_path = Path(path) / "kaggle_london_house_price_data.csv"

df = pd.read_csv(csv_path)
```

The dataset contains approximately 418,000 London residential property transactions spanning from 1995 to 2024, including:
- historical sale prices,
- structural housing characteristics,
- geographic coordinates,
- property types,
- tenure information,
- and energy ratings.

## Notebooks

The notebooks contain:
- full exploratory data analysis,
- preprocessing workflows,
- feature engineering,
- model experimentation,
- SHAP analysis,
- figures,
- outputs,
- and interpretation.

All outputs have been retained so the project can be reviewed without rerunning the notebooks.

---

## Conclusion

This project demonstrates that combining feature engineering, geographic information, ensemble machine learning, and segmented-market frameworks can produce commercially useful and interpretable predictive models for London residential property valuation.

