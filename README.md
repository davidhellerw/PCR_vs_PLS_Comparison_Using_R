<h1>Comparative Analysis of Principal Component Regression (PCR) and Partial Least Squares Regression (PLS) on Air Quality Data</h1>

<h2>Overview</h2>
<p>This project provides a comparative analysis of Principal Component Regression (PCR) and Partial Least Squares Regression (PLS) for predicting benzene (C6H6) concentrations using the Air Quality Dataset from the UCI Machine Learning Repository. The dataset contains measurements of various air pollutants and meteorological variables collected from an Italian monitoring station. The primary goal is to address multicollinearity and dimensionality reduction to improve predictive accuracy.</p>

<h2>Dataset</h2>
<p>The Air Quality Dataset includes:</p>
<ul>
  <li>Measurements of air pollutants: CO, NMHC, NOx, NO2, O3, and benzene (C6H6)</li>
  <li>Meteorological variables: Temperature, Relative Humidity (RH), Absolute Humidity (AH)</li>
  <li>Sensor responses for the pollutants</li>
</ul>
<p>The target variable for this analysis is the concentration of benzene (C6H6).</p>
<p>Link to the dataset: <a href="https://archive.ics.uci.edu/ml/datasets/Air+Quality">UCI Air Quality Dataset</a></p>

<h2>Methodology</h2>

<h3>Data Cleaning and Preparation</h3>
<ul>
  <li><strong>Handling Missing Values</strong>: Missing values were addressed by replacing them with the mean of each column.</li>
  <li><strong>Outlier Detection and Removal</strong>: Outliers were identified using the IQR method and removed to prevent skewed model results.</li>
  <li><strong>Scaling</strong>: All predictor variables were scaled to ensure they contribute equally to the models.</li>
</ul>

<h3>Exploratory Data Analysis (EDA)</h3>
<ul>
  <li><strong>Visualization</strong>: Created histograms and box plots to understand the distribution of the scaled variables and detect anomalies.</li>
</ul>

<h3>Modeling</h3>
<ul>
  <li><strong>Principal Component Regression (PCR)</strong>: Combines Principal Component Analysis (PCA) and linear regression. PCA was used to transform the predictors into a set of uncorrelated components, which were then used to fit the regression model.</li>
  <li><strong>Partial Least Squares Regression (PLS)</strong>: Simultaneously considers the predictor and response variables, extracting components that maximize the covariance between them.</li>
</ul>

<h3>Model Evaluation</h3>
<ul>
  <li><strong>Cross-Validation</strong>: Used to determine the optimal number of components for both PCR and PLS models.</li>
  <li><strong>Performance Metrics</strong>: Models were evaluated using Root Mean Squared Error (RMSE) and R-squared to compare predictive accuracy.</li>
</ul>

<h2>Results</h2>

<h3>Key Findings</h3>
<ul>
  <li><strong>PLS</strong>: Demonstrated superior predictive performance with an RMSE of 0.972 and an R-squared of 0.9744, effectively capturing the relationship between predictors and the response variable.</li>
  <li><strong>PCR</strong>: Provided valuable insights into the variance structure of predictors but had a slightly higher RMSE of 1.572 and an R-squared of 0.9331.</li>
  <li><strong>Optimal Number of Components</strong>: Both models showed optimal performance with about 5-6 components.</li>
</ul>

<h3>Conclusion</h3>
<ul>
  <li><strong>PLS</strong>: Recommended for predictive modeling due to its higher accuracy in predicting benzene concentrations.</li>
  <li><strong>PCR</strong>: Useful for exploratory data analysis and understanding the variance structure within predictors.</li>
</ul>

<h2>Tools and Libraries</h2>
<ul>
  <li><strong>Data Manipulation</strong>: dplyr, tidyr</li>
  <li><strong>Data Visualization</strong>: ggplot2, GGally</li>
  <li><strong>Modeling</strong>: pls, caret</li>
  <li><strong>Data Reading</strong>: readr</li>
  <li><strong>Time Handling</strong>: hms</li>
</ul>

<h2>Project Structure</h2>
<ul>
  <li><strong>Data</strong>: Contains the dataset and any preprocessing scripts.</li>
  <li><strong>Scripts</strong>: Includes R scripts for data cleaning, EDA, modeling, and evaluation.</li>
  <li><strong>Results</strong>: Stores the results of the analyses, including visualizations and model performance metrics.</li>
  <li><strong>README</strong>: Comprehensive project overview and instructions.</li>
</ul>
