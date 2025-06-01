# Python Data Structures and Analysis - Module 1

## Arrays and Lists

```python
# To create an array
array = [1,2,3,4]
print(array)
```

## DataFrames with Pandas

```python
# To define a dataframe
import pandas as pd
mca = {'col1': [1,2,3,4,5], 'col2': [4,5,6,7,8]}
df = pd.DataFrame(mca)
print(df)
```

```python
# To count the number of columns in the dataframe
print(len(df.columns))
```

```python
# To count the number of rows in dataframe
print(len(df.index))
```

```python
# To display only top 5 rows using head()
import pandas as pd
df = pd.read_csv('https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info.csv')
print(df.head())
```

```python
# To display all rows accept last 2 rows
import pandas as pd
df = pd.read_csv('https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info.csv')
print(df.head(-2))
```

## Array Operations

```python
# To find the maximum value in the array
print(max(array))
```

```python
# To find the minimum value in the array
print(min(array))
```

```python
# To find the average value in the array
import numpy as np
arr = [1,2,3]
avg = np.mean(arr)
print(avg)
```

## Data Import and Reading CSV Files

```python
# To import data using python
import pandas as pd
df = pd.read_csv('https://raw.githubusercontent.com/Saniyaj21/da-csv/refs/heads/main/info.csv')
print(df)
```

## Data Type Conversion in DataFrames

```python
import pandas as pd

# Creating demo mca DataFrame with string values
data = {
    'Average_Pulse': ['85', '90', '78', '88'],
    'Max_Pulse': ['120', '130', '115', '125']
}

mca = pd.DataFrame(data)

# Before conversion
print("Before Conversion:")
print(mca)

# Convert to float
mca['Average_Pulse'] = mca['Average_Pulse'].astype(float)
mca['Max_Pulse'] = mca['Max_Pulse'].astype(float)

# After conversion
print("\nAfter Conversion:")
print(mca)
```

## Data Summary Statistics

```python
# To summaring data using describe()
data = {
    'Average_Pulse': ['85', '90', '78', '88'],
    'Max_Pulse': ['120', '130', '115', '125']
}
data = pd.DataFrame(data)
print(data.describe())
```