# DataFrames

## Watch this video to see the basics in action!
<iframe width="560" height="315" src="https://www.youtube.com/embed/eeuFiAb5tBY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

DataFrames are used very commonly when analyzing data, so it is a useful concept to understand! A "DataFrame is a 2-dimensional data structure with columns of potentially different types" ([Pandas - Intro to data structures](https://pandas.pydata.org/pandas-docs/stable/user_guide/dsintro.html#:~:text=DataFrame%20is%20a%202%2Ddimensional,most%20commonly%20used%20pandas%20object.)). 

## Creating a DataFrame

General template for creating a `DataFrame`: 

First we need to import pandas. 

```python
import pandas as pd
```

Then, we can construct the dataframe itself. 

```python
data = {'Column 1 Name': ['Value 1','Value 2',...],
        'Column 2 Name': ['Value 1', 'Value 2', ...],
        ...
        }
        
df = pd.DataFrame(data)
```

Simple example with output: 

```python
data = {'Name': ['Luke','Leia'], 'Age': [19, 19]}
df = pd.DataFrame(data)
df
```
       Name  Age
    0  Luke  19
    1  Leia  19


The first column, with the numbers starting at $0$ represent the index. If a specific index is wanted, it can be assigned with the `DataFrame` is created. 

## Getting Data from DataFrame

Assuming the same dataframe from above, we can obtain the names from the dataframe with the following: 

``` python
df.Name
```

    0  Luke
    1  Leia
   
Using a logical mask, we can obtain the row of the dataframe where the name is Luke. This could be done for any of the values or columns in the dataframe if you are looking for something specific. 

```python
df[df.Name=='Luke']
```
       Name  Age
    0  Luke  19
    
## Adding Columns to DataFrame

We want to add a gender column, which we tell it what values to add for Luke and Leia. 
```python
df['Gender'] = ['Male','Female']
df
```
         Name   Age    Gender
     0   Luke   19     Male
     1   Leia   19     Female
     
## Describing Data

To get some basic information regarding the values in the columns of the dataframe, we can use `describe()`. 

```python
df.describe()
```
            Age
    count   2.0
    mean   19.0
    std     0.0
    min    19.0
    25%    19.0
    50%    19.0
    75%    19.0
    max    19.0
    
With additional data added to the dataframe, this analysis will become more interesting and valuable! 

## Attributes and Methods

There are a number of attributes and methods to be utilized with DataFrames. Resources for those can be found [here](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.html). Additionally, some of these attributes and methods will be shown through the examples provided. 
