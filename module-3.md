# Data Analysis with Python - Module 3

## Loading and Examining the Dataset

```python
# To get the summary data from the info3.csv
import pandas as pd
df = pd.read_csv('https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info3.csv')
```

## Calculating Percentiles

```python
# To calculate 10% percentile for the Max_pulse in info3.csv
import numpy as np
percentile_10 = np.percentile(df['Max_Pulse'], 10)
print(percentile_10)
```

```python
# To calculate 25% percentile for the Average_pulse in info3.csv
import numpy as np
percentile_25 = np.percentile(df['Average_Pulse'], 25)
print(percentile_25)
```

## Statistical Analysis - Standard Deviation

```python
# To find the standard deviation for every attributes in info3.csv
sd = np.std(df)
print(sd)
```

```python
# To find the co-efficient variation of every attributes in info3.csv
sd = np.std(df)
cv = sd / np.mean(df)
print(cv)
```

## Variance Analysis

```python
# To calculate the varience of Average_Pulse
sd = np.std(df['Average_Pulse'])
var = np.var(df['Average_Pulse'])
print(var)
```

## Correlation Analysis

```python
# To display an example of a linear relationship (correlation coefficient)
import matplotlib.pyplot as plt
df.plot(x = "Average_Pulse", y = "Calorie_Burnage", kind = "scatter")
plt.show()
```

```python
# To plot perfect regative_correlation using a dataframe
import matplotlib.pyplot as plt
import pandas as pd
regative_correlation = {
    'x':[10,8,6,4,2],
    'y':[20,40,60,80,100]
}
df = pd.DataFrame(regative_correlation)
df.plot(x = "x", y = "y", kind = "scatter")
plt.show()
```

```python
# To plot no corerelation using a dataframe info3.csv
import matplotlib.pyplot as plt
import pandas as pd
info3 = pd.read_csv('https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info3.csv')
info3.plot(x = "Duration", y = "Max_Pulse", kind = "scatter")
plt.show()
```

## Correlation Matrix Analysis

```python
# to print correlation matrix (tabular representation using info3.csv)
corr_matrix = round(info3.corr(), 2)
print(corr_matrix)
```

```python
# To genarate heatmap (graphical representations using info3.csv)
import seaborn as sns
import matplotlib.pyplot as plt
corr_matrix = round(info3.corr(), 2)
sns.heatmap(corr_matrix, annot = True)
plt.show()
```