# Real-Estate-Pricing
**Real Estate Pricing**

I know a lot of people who are looking for homes in NYC right now so I was curious to see whether ML models could predict the price of homes sold. I also wanted to use regression models and techniques such as elastic net and lasso (L1) regression.
This project predicts the sales of real estate using regression models. 

**Nulls**
The original source of the dataset highlighted the variables that used NULLs to mean 'None'.
So, the nulls in those variables were replaced with 'None' while some of the Nulls were replaced with the median value of the variable in relation to other correlated fields.

**Outliers**
Outliers were capped based on the IQR for the independent variables

**Normalization:**
Log Normalised the target variable (Sales Price) in the dataset in order to standard the data and ensure the model returns positive values for models like linear regression. Log normalising aids when the standard deviation/variance or values in the variable are large. In addition, it also aids when the distribution the variable has a skewed distribution. In this case, the distribution was left skewed. So, Log normalization served as a variance stablizing transformer for the variable. It also aids in diminishing the influence of outliers on the performance of the models. 

**Modeling:**
Used a pipelined linear regression model with elasticNet and Lasso regularization. A XGBRegressor model was also applied on the data as well. The evaluation metrics used were root mean squared error and mean squared error. Cross validation 5-Kfold was used to confirm the results of the model by splitting the data into 5 folds.

**References: **
https://www.manageengine.com/products/eventlog/logging-guide/log-normalization.html#:~:text=Log%20normalization%20is%20the%20process,into%20consistent%20representations%20and%20categorizations.

https://medium.com/analytics-vidhya/log-transform-for-positivity-d3e1f183c804
