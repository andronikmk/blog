---
title: "U.K. Economic Data Dash App"
date: "2020-02-04"
template: "project"
draft: false
slug: "uk-economic-data-dash-app"
category: "Machine Learning"
tags:
  - "machine learning" 
  - "logisitc regression"
description: "A Plotly Dash app used real consumer earnings and consumer price index on a millennium of macroeconomic data from the Bank of England"
socialImage: "/media/image-3.jpg"
---
[![Alt text](/media/icons/GitHub-Mark-32px.png)](https://github.com/andronikmk/uk-data-dash-app)

## Introduction

<p style="text-align: justify;"> 
The economic development of Europe proceeded political consolidation and differentiation. As large sovereignties emerged and state regulation superseded guild and municipal regulation, economic development could extend freely over a wider territories. Between 1270 and 1870 England and Great Britain slowly progressed from the periphery of the European economy to centre-stage of an integrated global economy. In the process Britain escaped the Malthusian trap and by the eighteenth century had successfully reconciled a rising population with a rising standard of living.
The following is a short article and demo which explores data published by the Bank of England. The <a href="https://fred.stlouisfed.org/release?rid=389">dataset</a> contains a broad set of macroeconomic and financial indicators from England and Great Britain stretching back to the 13th century.
</p>

<figure>
	<img src="/media/uk-economic-data-dash-app/uk1.png">
	<figcaption>Real GDP, Real GDP per head, Population</figcaption>
</figure>

<figure>
	<img src="/media/uk-economic-data-dash-app/image4.png">
</figure>

## Model and Metric

<p style="text-align: justify;"> 
Real consumption earnings was modeled using a decision tree regressor which breaks down a data-set into smaller and smaller subsets while at the same time an association tree is incrementally developed. This method of analysis resulted in a validation accuracy of 0.641 which suggests that the percentage of correct classifications using this model was approximately 64.1%.
</p>

```python
# imported libraries
from sklearn.impute import SimpleImputer
from sklearn.pipeline import make_pipeline
from sklearn.tree import DecisionTreeRegressor

# target
target = 'Real_consumption_earnings_Growth_GB'

# drop target feature
train_features = train.drop(columns=[target,'Growth_consumption_earnings','Consumer_price_inflation'])

# get list of numeric features
numeric_features = train_features.select_dtypes(include='number').columns.tolist()

# combine numeric features
features = numeric_features

# Arrange data into X features matrix and y target vector 
X_train = train[features]
y_train = train[target]
X_val = val[features]
y_val = val[target]
X_test = test[features]

# pipeline
pipeline = make_pipeline(
    SimpleImputer(missing_values=np.nan , strategy='median'),
    DecisionTreeRegressor(max_depth=2)
)

# pipeline fit and validtion score
pipeline.fit(X_train, y_train)
print('Validation Accuracy', pipeline.score(X_val, y_val))
```

<figure>
	<img src="/media/uk-economic-data-dash-app/image3.png">
	<figcaption>Prediction</figcaption>
</figure>




## Presentation

+ [U.K. Data Dash App](https://uk-data-dash-app.herokuapp.com/)


