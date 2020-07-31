## Project motivation
In the trend of online shopping malls replacing traditional malls, more and more people are getting interested in becoming online seller. This project is focused on clients who are interested in finding the characteristics of product postings that might increase the sale of their products. The data used for this project is the query results of typing 'keyboard' in ebay.com.

## Findings
#### A few meaningful yet intuitive inferences about the features in the model came to several findings/recommendations for clients:
- Sale rate tends to decrease faster as the price increases when there is shipping cost more than \\$10
- Free return and writing a product review has highly positive impact on the sale rate

## Organization of the submission files
#### There are 4 ipython notebook files in the submission directory
- ebay_scraper.ipynb
- clean_data.ipynb
- feature_engineering.ipynb
- regression_modeling.ipynb
*At the top of each file has a brief description about the codes*

## Data Analysis
With initial datasets cleaned, there were 5211 observations which were split into train-val-test for cross validation. Distribution plots, Scatter plots, and Correlation plots were frequently used for feature-engineering. With the engineered dataset, two models were trained: Linear Regression with log-transformed target and Poisson regression. The two models were compared using cross validation results and lastly, regularized Poisson regression was selected. After the model has been selected, plots to measure the model's predictive power and interaction effects were investigated. The model's estimated parameters were used for making inferences about the effect of features on the target.

## Design Decisions
#### Feature-engineering
- The individual features were transformed using the scatter plot between the target and each feature.
- Interaction effects between numeric variable and dummy variable were investigated using the line plots.
#### Selection
- Variables that suffered high collinearity with other feature (>95%) were removed manually to avoid overfitting
- Through regularization, the number of variables reduced down from 19 to 4.

## Sources
[1] Broadening Your Statistical Horizons,
Generalized Linear Models and Multilevel Models,
Julie Legler and Paul Roback,
2019-01-29. URL: https://bookdown.org/roback/bookdown-bysh/ch-poissonreg.html#sec-PoisResid
<br>
[2] Regression Challenge: Day 2 - Python,
Python notebook using data from 2017 Kaggle ML & DS Survey,
URL: https://www.kaggle.com/mryder73/regression-challenge-day-2-python
<br>
[3] Azur MJ, Stuart EA, Frangakis C, Leaf PJ. Multiple imputation by chained equations: what is it and how does it work?. Int J Methods Psychiatr Res. 2011;20(1):40-49. doi:10.1002/mpr.329. URL: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3074241/
<br>
[4] eBay query results of 'keyboard'. https://www.ebay.com/sch/i.html?_from=R40&_nkw=keyboard
<br>
Python Packages:
<br>
requests<br>
bs4<br>
numpy<br>
fake_useragent<br>
time<br>
pandas<br>
patsy<br>
statsmodels.api<br>
statsmodels.formula.api<br>
statsmodels.compat.python<br>
scipy<br>
seaborn<br>
matplotlib.pyplot<br>
sklearn.linear_model<br>
sklearn.pipeline<br>
sklearn.preprocessing<br>
sklearn.model_selection<br>
statsmodels.imputation<br>
statsmodels.graphics.factorplots<br>
