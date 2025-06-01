# Data Analysis with Python - Module 2

## Loading the Dataset

```python
# to import dataset (info2.csv)
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info2.csv")
df
```

## Data Visualization

```python
# To plot a straight line using dataset
import matplotlib.pyplot as plt
df.plot(x='Average_Pulse', y = 'Calorie_Burnage', kind='line')
plt.ylim(ymin = 30)
plt.xlim(xmin = 50)
plt.show()
```

## Custom Functions for Data Analysis

```python
# write a user define function to calculate slope
def slope(x1, y1, x2, y2):
    s = (y2-y1)/(x2-x1)
    return s

print(slope(80, 240, 85, 250))
```

## Linear Regression Analysis

```python
# Calculate slope and intercept using polyfit
import numpy as np
import pandas as pd

df = pd.read_csv("https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info2.csv")
x = df['Average_Pulse']
y = df['Calorie_Burnage']

slope_intercept = np.polyfit(x, y, 1)

print(slope_intercept)
```

```python
# User defined function to calculate Calorie_Burnage
def Calorie_Burnage(x1, slope = 2, intercept = 80):
    s = slope * x1 + intercept
    return s

print(Calorie_Burnage(125))
```

## Scatter Plot Analysis

```python
# Write code to scatter values monitoring min and max limit
import matplotlib.pyplot as plt
import pandas as pd

df = pd.read_csv("https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info2.csv")
df.plot(x = 'Average_Pulse', y = 'Calorie_Burnage', kind = 'scatter')
plt.show()
```