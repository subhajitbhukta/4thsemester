# Linear Regression Analysis of Health Data

## Basic Linear Regression

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Reading the dataset
health_info = pd.read_csv('https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info3.csv')

# Performing linear regression
from scipy import stats
x = health_info['Average_Pulse']
y = health_info['Calorie_Burnage']
slope, intercept, r, p, std_err = stats.linregress(x, y)

# Printing regression statistics
print("slope", slope)
print("intercept", intercept)
print("correlation coefficient", r)
print("pvalue", p)
print("standard error", std_err)

# Creating the regression line function
def myfunc(x):
    return slope * x + intercept

# Calculating predicted values
new_y = list(map(myfunc, x))
print(new_y)

# Plotting the data and regression line
plt.scatter(x, y)
plt.plot(x, new_y)
plt.ylim(ymin=0, ymax=2000)
plt.xlim(xmin=0, xmax=200)
plt.xlabel('Average_Pulse')
plt.ylabel('Calorie_Burnage')
plt.show()
```

## Linear Regression using Statsmodels

```python
import statsmodels.formula.api as smf

# Reading the dataset (using the same data as above)
health_info = pd.read_csv('https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info3.csv')

# Creating and fitting the model
model = smf.ols("Calorie_Burnage ~ Average_Pulse", data=health_info)
result = model.fit()

# Displaying the detailed statistical summary
print(result.summary())
```