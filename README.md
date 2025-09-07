# energy-demand-week2
<h1 align="center">⚡ Urban Energy Demand Forecasting – Week 2 Submission</h1>

<p align="center">
   <img src="https://img.shields.io/badge/Python-3.11-blue?logo=python" alt="Python">
   <img src="https://img.shields.io/badge/LightGBM-GradientBoosting-green" alt="LightGBM">
   <img src="https://img.shields.io/badge/Platform-Jupyter%20Notebook-orange?logo=jupyter">
</p>

<hr>

<h2>📌 Project Overview</h2>
<p>This repository contains the <b>Week 2 submission</b> for forecasting urban electricity demand. The goal is to predict energy consumption using <b>historical data</b> and <b>machine learning</b>, focusing on <b>LightGBM regression</b>.</p>
<p>This work serves as a <b>snapshot</b> for Week 2. Further improvements and feature engineering will be implemented in Week 3.</p>

<hr>

<h2>🗂 Folder Contents</h2>
<table>
<tr><th>File/Folder</th><th>Description</th></tr>
<tr><td><code>Week2_LightGBM.ipynb</code></td><td>Jupyter Notebook with data preprocessing, modeling, evaluation, and plots</td></tr>
<tr><td><code>plots/</code></td><td>Time-series visualizations of actual vs predicted energy demand</td></tr>
<tr><td>Any CSV or helper files</td><td>Required for running the notebook</td></tr>
</table>

<hr>

<h2>⚙️ Approach</h2>
<h3>1. Data Preprocessing</h3>
<ul>
  <li>Filled missing numeric values with <b>median</b>, categorical with <b>mode</b></li>
  <li>Basic data cleaning to prepare for modeling</li>
</ul>

<h3>2. Modeling</h3>
<ul>
  <li><b>LightGBM Regressor</b> with reasonable hyperparameters:</li>
</ul>
<pre>
n_estimators: 500
learning_rate: 0.05
max_depth: 10
num_leaves: 50
min_child_samples: 20
subsample: 0.8
colsample_bytree: 0.8
</pre>
<ul>
  <li>Planned hyperparameter tuning via <b>RandomizedSearchCV</b></li>
  <li>Implemented <b>early stopping</b> to prevent overfitting</li>
</ul>

<h3>3. Evaluation</h3>
<table>
<tr><th>Metric</th><th>Value</th></tr>
<tr><td>MAE</td><td>~18.5</td></tr>
<tr><td>RMSE</td><td>~25.7</td></tr>
<tr><td>R²</td><td>~0.31</td></tr>
</table>
<p>Visualized <b>Actual vs Predicted demand</b> using time-series plots</p>

<hr>

<h2>📊 Observations</h2>
<ul>
  <li>Model captures overall trends but misses some peaks</li>
  <li>Indicates <b>moderate predictive performance</b></li>
  <li>Further improvements (Week 3):
    <ul>
      <li>Time-series features: hour, day, lag, rolling statistics</li>
      <li>Full hyperparameter tuning</li>
      <li>Deployment considerations</li>
    </ul>
  </li>
</ul>

<hr>

<h2>📝 Notes</h2>
<ul>
  <li>This submission is a <b>Week 2 snapshot</b></li>
  <li>Code is fully reproducible via the Jupyter Notebook</li>
</ul>

<hr>

<h2>🚀 Next Steps (Week 3)</h2>
<ol>
  <li>Add advanced <b>time-series features</b></li>
  <li>Refine LightGBM <b>hyperparameters</b></li>
  <li>Evaluate on additional test scenarios</li>
  <li>Prepare final report and deployment-ready model</li>
</ol>
