# CodeAlpha_task4
# Sales Prediction using Python
**CodeAlpha Data Science Internship — Task 4**

Predicting product sales based on advertising spend across **TV**, **Radio**, and **Newspaper** channels using regression models, with actionable business insights for marketing strategy.

## Dataset
`data/advertising.csv` — 200 records with the following columns:
| Column | Description |
|---|---|
| TV | Advertising spend on TV (in thousands) |
| Radio | Advertising spend on Radio (in thousands) |
| Newspaper | Advertising spend on Newspaper (in thousands) |
| Sales | Product sales (in thousands of units) |

## Objective
- Clean and explore the data
- Visualize relationships between ad spend and sales
- Engineer features (total spend, channel share, TV×Radio interaction)
- Train and compare regression models (Linear Regression, Random Forest)
- Evaluate with MAE, RMSE, R², and cross-validation
- Extract business insights on advertising strategy

## Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

## Project Structure
```
sales_prediction/
├── data/
│   └── advertising.csv
├── outputs/
│   ├── correlation_heatmap.png
│   ├── spend_vs_sales.png
│   ├── sales_distribution.png
│   ├── actual_vs_predicted.png
│   └── feature_importance.png
├── sales_prediction.py
└── README.md
```

## How to Run
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
python sales_prediction.py
```

## Results
| Model | MAE | RMSE | R² (test) | R² (5-fold CV) |
|---|---|---|---|---|
| Linear Regression | 0.36 | 0.45 | 0.994 | 0.988 |
| Random Forest | 0.46 | 0.59 | 0.989 | 0.988 |

**Best model: Linear Regression** — near-perfect fit once the TV×Radio interaction term is included, confirming a strong linear (with synergy) relationship between ad spend and sales.

## Business Insights
- **TV** advertising has the strongest correlation with sales (r ≈ 0.78) — it's the primary sales driver.
- **Radio** shows a moderate positive effect (r ≈ 0.58) and works especially well in combination with TV.
- **Newspaper** has the weakest correlation (r ≈ 0.23) — spend here has limited impact on sales.
- **Recommendation:** Shift budget away from Newspaper toward TV and Radio. Running TV and Radio campaigns together produces a synergistic lift greater than either channel alone.

