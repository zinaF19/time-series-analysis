# Time Series Analysis

A hands-on introduction to time series analysis and forecasting. Five core notebooks build a complete classical-forecasting toolkit, from representing a series in pandas to evaluating SARIMA forecasts, and an optional sixth notebook adds the machine-learning perspective with XGBoost. All datasets are classic real-world series (air passengers, CO2, sunspots, electrical equipment orders) fetched at run time from statsmodels.

## Learning Objectives

By the end of this repository, you should be able to:

- Represent a time series as a pandas `Series` with a `DatetimeIndex` and resample it to a different frequency.
- Identify trend, seasonality, and autocorrelation using line, seasonal, lag, and ACF/PACF plots.
- Decompose a series into trend, seasonal, and residual components and apply moving averages and exponential smoothing.
- Test for stationarity with ADF and KPSS, difference a series, and fit AR, MA, and ARIMA models.
- Build a time-series train/test split and compare baseline, Holt-Winters, and SARIMA forecasts with MAE, RMSE, and MAPE.
- Engineer lag and calendar features to forecast with XGBoost and compare it like for like against the classical models.

## Learning Path

Work through the notebooks in this order:

| File / Folder | Description |
|---|---|
| [**01 - What Is a Time Series**](01_what_is_time_series.ipynb) | Time-series properties, frequency, the forecasting task, and pandas representation. |
| [**02 - EDA and Visualization**](02_eda_and_visualization.ipynb) | Loading, resampling, and diagnosing a series with line, seasonal, lag, and ACF/PACF plots. |
| [**03 - Decomposition and Smoothing**](03_decomposition_and_smoothing.ipynb) | Trend, seasonal, and residual components; moving averages and exponential smoothing. |
| [**04 - Stationarity and ARIMA**](04_stationarity_and_arima.ipynb) | ADF and KPSS tests, differencing, and AR, MA, and ARIMA models. |
| [**05 - Forecasting and Evaluation**](05_forecasting_and_evaluation.ipynb) | Train/test splits, baselines, Holt-Winters and SARIMA, error metrics, and rolling-origin cross-validation. |
| [**06 - XGBoost for Time Series**](06_xgboost_for_time_series.ipynb) | Optional ML extension: forecast with lag and calendar features, see why tree models cannot extend a trend beyond the training data, and compare the results against the classical models. |

> [!NOTE]
> Notebooks 1 to 5 form a complete classical-forecasting curriculum. Notebook 6 is an optional machine-learning extension and is not a prerequisite for anything else.

### Additional Folders and Files

| File / Folder | Description |
|---|---|
| [**Solutions**](solutions/) | Reference solutions. |
| [**pyproject.toml**](pyproject.toml) | Project metadata and dependencies. |
| [**uv.lock**](uv.lock) | Locked dependency versions for reproducible installs. |

## Setup

> [!NOTE]
> Throughout these steps, text in angle brackets like `<repo-name>` is a **placeholder**. Replace it including the `< >` brackets with your own value. For example, `cd <repo-name>` becomes `cd ds-time-series-analysis`.

### 1. Create the Repository from the Template

Click **Use this template** on GitHub.

When creating the repository:

- Set yourself as the **Owner**
- Choose a repository name
- Disable **Include all branches**
- Click **Create repository**

> [!IMPORTANT]
> If you are working in pairs or groups, only **one person** should complete this step.

---

### 2. Add Collaborators (Pairs/Groups Only)

If working with teammates:

1. Open the repository on GitHub
2. Go to **Settings → Collaborators**
3. Add your teammates as collaborators
4. Share the repository link with your team

Teammates should accept the invitation before continuing.

---

### 3. Clone the Repository

Copy the SSH URL from the **Code** button on GitHub, then run:

```bash
git clone <copied-ssh-url>
```

The copied SSH URL will look like `git@github.com:<your-username>/<repo-name>.git`.

---

### 4. Move into the Project Folder and Install Dependencies

Move into the project folder, then install the dependencies with uv. This creates a `.venv` and installs everything pinned in `pyproject.toml` and `uv.lock`.

```bash
cd <repo-name>
uv sync
```

---

### 5. Open the Notebooks

> [!NOTE]
> Make sure you open VS Code from the project root so it automatically detects the `.venv` environment you just created.

Launch VS Code in the project root folder:

```bash
code .
```

Then open a notebook and select the `.venv` Python environment as the kernel.

> [!NOTE]
> The notebooks download their datasets from statsmodels at run time.
## References & Further Reading

- [**Forecasting: Principles and Practice (FPP3)**](https://otexts.com/fpp3/): The free online textbook by Hyndman and Athanasopoulos that grounds every notebook.
- [**Pandas: Time Series Functionality**](https://pandas.pydata.org/docs/user_guide/timeseries.html): User guide for `DatetimeIndex`, resampling, and shifting.
- [**Statsmodels: Time Series Analysis**](https://www.statsmodels.org/stable/tsa.html): API reference for the decomposition, smoothing, and ARIMA tools used in notebooks 3 to 5.
- [**pmdarima Documentation**](https://alkaline-ml.com/pmdarima/): Python port of R's `auto.arima` for automated order selection.
- [**XGBoost Documentation**](https://xgboost.readthedocs.io/en/stable/): Official documentation for the gradient-boosting library used in notebook 6.
- [**M5 Forecasting Competition on Kaggle**](https://www.kaggle.com/competitions/m5-forecasting-accuracy): Large-scale retail forecasting in practice, with community notebooks comparing classical and ML approaches.
