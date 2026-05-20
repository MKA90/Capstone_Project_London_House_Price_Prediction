# Predicting London House Prices Using Machine Learning

This project explores how machine learning can be used to predict historical residential property prices across the London housing market using structural, geographic, temporal, and historical transaction data.

Using over 418,000 London property transactions spanning from 1995–2024, the project investigates:
- exploratory data analysis (EDA),
- feature engineering,
- ensemble machine learning,
- inflation-adjusted modelling,
- segmented market modelling,
- and SHAP-based model interpretability.

The overall aim of the project was not simply to maximise predictive accuracy, but also to better understand the economic and geographic factors driving London property prices within one of the world’s most heterogeneous housing markets.

---

## Key Highlights

- Built machine learning models using over 418,000 London property transactions
- Developed segmented-market Random Forest models for improved predictive performance
- Engineered structural, spatial, and temporal housing features
- Investigated inflation-adjusted versus nominal-price modelling
- Applied SHAP analysis to improve model interpretability
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
- Inflation-adjusted modelling showed that nominal-price models relied heavily on long-term market appreciation trends.
- Geographic variables, floor area, and proximity to Central London emerged as some of the strongest drivers of predicted property prices.
- SHAP analysis demonstrated that different housing-market segments relied on different predictive drivers.

---

## Project Contents

This repository contains:
- a full exploratory data analysis notebook,
- the complete machine learning modelling pipeline,
- the final capstone report,
- and supporting datasets used throughout the project.

The notebooks include:
- preprocessing workflows,
- feature engineering,
- model experimentation,
- SHAP analysis,
- figures and outputs,
- and written interpretation throughout.

All notebook outputs have been retained so the project can be reviewed without rerunning the code.

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

The main dataset used in this project is the Kaggle dataset:

**London House Price Data** by Jake Wright.

The project also incorporates UK inflation (CPI) data for the inflation-adjusted modelling experiments.

The combined datasets contain approximately 418,000 London residential property transactions spanning from 1995 to 2024, including:
- historical sale prices,
- structural housing characteristics,
- geographic coordinates,
- property types,
- tenure information,
- energy ratings,
- and inflation data used for CPI-adjusted price modelling.

The housing dataset was downloaded directly using `kagglehub`:

```python
path = kagglehub.dataset_download("jakewright/house-price-data")

csv_path = Path(path) / "kaggle_london_house_price_data.csv"

df = pd.read_csv(csv_path)
```

---

## Conclusion

This project demonstrates that combining feature engineering, geographic information, ensemble machine learning, and segmented-market frameworks can produce commercially useful and interpretable predictive models for London residential property valuation.

The project also highlights the challenges associated with modelling highly heterogeneous real-estate markets and the importance of balancing predictive accuracy with economic interpretability.

