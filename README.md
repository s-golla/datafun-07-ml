# datafun-07-ml

This repository contains the coursework notebook and supporting files for the DataFun Module 7 exercises. The primary deliverable is the notebook `sgolla_ml.ipynb` that implements the guided projects: Part 1 (line), Part 2 (SciPy linregress), Part 3 (scikit-learn), Part 4 (insights & communication), and an optional Part 5 (California Housing bonus).

## What's in this repo
- `sgolla_ml.ipynb` — main Jupyter notebook with Parts 1–5 (run this).  
- `data/` — data files used by the notebook (for example `ave_hi_nyc2_jan_1895-2018.csv`).
- `requirements.txt` — Python dependencies used by the notebook and experiments.

## Quick start (Windows / PowerShell)
1. Open the project folder in VS Code (recommended).
2. Create and activate a Python virtual environment (recommended):

    ```powershell
    python -m venv .venv; .\.venv\Scripts\Activate.ps1
    ```

3. Install dependencies:

    ```powershell
    pip install -r requirements.txt
    ```

4. Start Jupyter and open the notebook:

    ```powershell
    jupyter lab
    # or
    jupyter notebook
    ```

5. Open `sgolla_ml.ipynb` and run the notebook cells in order (or use Kernel → Restart & Run All).

Notes:
- The notebook includes an explicit data-acquisition cell that loads `data/ave_hi_nyc2_jan_1895-2018.csv` when present; if that CSV is missing the notebook creates a small demo DataFrame so the flows remain runnable.
- Part 5 uses scikit-learn's California Housing dataset (fetched locally via scikit-learn) and trains multiple regression models.

## Notebook structure (high level)
- Introduction: Title, author, and repository link.
- Part 1 — Chart a Straight Line: Celsius vs Fahrenheit example to explain y = mx + b.
- Part 2 — Prediction (SciPy):
  - Data acquisition: loads `data/ave_hi_nyc2_jan_1895-2018.csv` when available.
  - Cleaning & inspection, descriptive statistics.
  - Fit line with `scipy.stats.linregress` and predict 2024.
  - Plot data and best-fit line.
- Part 3 — Prediction (scikit-learn):
  - Train/test split, fit `LinearRegression`, evaluate and predict 2024.
  - Plot train/test points and fitted line.
- Part 4 — Insights & Communication: technical insights and guidance on presenting results to stakeholders.
- Part 5 — Bonus (California Housing):
  - Load the California Housing dataset, train four regressors (LinearRegression, DecisionTree, RandomForest, GradientBoosting), compare R^2 / RMSE, and visualize best-model predictions.

## Reproducibility & environment
- Use the `requirements.txt` provided to create a reproducible environment. If you change the environment, update the requirements file.
- The notebook includes a cell that prints versions for Python, pandas, numpy, seaborn, scipy, and scikit-learn — include these when you share results for reproducibility.

## Tips for presentation and storytelling
- Start with the question: what are you predicting and why it matters.  
- Summarize data and cleaning steps succinctly.  
- Present model results (slope, intercept, r, r^2, std_err, MSE, RMSE) and show uncertainty or caveats.  
- Include visualizations with clear axis labels, annotations for key takeaways (for example the predicted 2024 point), and a one-line summary conclusion.

## Commit & push changes
When you're ready to save notebook edits:

```powershell
git pull
git add sgolla_ml.ipynb
git commit -m "Update notebook: Part X changes / add Part 5 bonus"
git push
```
