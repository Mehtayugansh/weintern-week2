# Walmart Sales Forecasting — Assignment README

## Project overview
This project contains three tasks based on the Walmart Store Sales Forecasting dataset:
1. Data Cleaning
2. Exploratory Data Analysis (EDA)
3. Sales Prediction Model

## Recommended folder structure
walmart-recruiting-store-sales-forecasting/
- Task 1/ (datasets, notebooks, outputs, reports)
- Task 2/ (datasets, notebooks, outputs, reports)
- Task 3/ (datasets, notebooks, outputs, reports)
- README.md

## Requirements
Python 3.x with pandas, numpy, matplotlib, seaborn, scikit-learn, and Jupyter.

Install:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

## How to run
1. Put the original Kaggle dataset files in the appropriate Task 1 datasets folder.
2. Open Jupyter Notebook and open each notebook from its `notebooks` folder.
3. Run notebooks from top to bottom in order: Task 1, Task 2, then Task 3.
4. Check that each notebook's file paths point to the correct project folders.
5. Confirm that Task 1 creates `walmart_cleaned_merged.csv` where Task 2 and Task 3 expect it.
6. Save the notebooks after all cells run successfully.
7. Export the completed Task 2 notebook to PDF, as required by the assignment.
8. Keep charts, CSV tables, reports, and required datasets in their corresponding folders.

## Task 3 recorded model results

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 1703.62 | 3319.16 | 0.9772 |
| Random Forest | 1431.62 | 3104.46 | 0.9800 |
| Tuned Random Forest | 1506.59 | 3242.77 | 0.9782 |

The original Random Forest had the best recorded test metrics. It was trained on a 100,000-row sample, while Linear Regression used the full training set. Hyperparameter tuning used a 20,000-row randomly selected sample sorted by date; this is a limitation because it is not a continuous chronological sample.

## Important limitations to disclose
- Lag features use earlier observed sales. The evaluation represents rolling forecasting where previous actual sales are available for later predictions.
- Early store-department records without enough history were removed.
- Markdown columns are sparse; tuning produced warnings where some folds had no observed values in those columns.
- Feature importance is relative predictive importance and does not demonstrate causation.
- Metrics describe this held-out test period and do not guarantee future performance.

## Submission checklist
- [ ] Task 1 notebook (`.ipynb`)
- [ ] Original raw dataset files
- [ ] Cleaned output CSV
- [ ] Task 1 cleaning report
- [ ] Task 1 before/after data-quality comparison table
- [ ] Task 2 notebook (`.ipynb`)
- [ ] At least five labeled charts with descriptions
- [ ] Task 2 written insights and conclusions
- [ ] Task 2 PDF export
- [ ] Task 3 notebook (`.ipynb`)
- [ ] Task 3 model comparison CSV
- [ ] Actual-vs-predicted chart
- [ ] Random Forest feature-importance chart
- [ ] Hyperparameter tuning results
- [ ] Task 3 performance summary and limitations
- [ ] This README
- [ ] All required files uploaded to the assigned Google Drive folder

## Reproducibility note
These are the results recorded during development. Run each notebook from top to bottom before submission and update any results that change.
