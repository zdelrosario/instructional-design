# pandas Quick Syntax Glossary


<!-- toc -->
- [apply](#apply)
- [columns](#columns)
- [DataFrame](#DataFrame)
- [iloc](#iloc)
- [iterrows](#iterrows)
- [merge](#merge)
- [read_csv](#read_csv)
- [read_excel](#read_excel)
- [shape](#shape)


____

# apply

# columns
```python
my_columns = my_dataframe.columns
```

# DataFrame
```python
data = {
    'formula': ['MgAl2O4', 'Si3N4', 'Al2O3'],
    'mass (g)': [1.5, 1.3, 1.6],
    '%wt loss': [2.4, 2.0, 2.6]
}

my_dataframe = pandas.DataFrame(data)
```

# iloc
```python
cell_value = my_dataframe.iloc[rowIndex, colIndex]
```

# iterrows
```python
for rowIndex, rowData in my_dataframe.iterrows():
    print(f'Row Index: {rowIndex}')
    print(f'My Column Name: {rowData["My Column Name"]}')
```

# merge
```python
# like column names
new_dataframe = my_dataframe.merge(dataframe2, 
                                    how="<left, outer, inner, right>",
                                    on="column_name")
```

```python
# unlike column names
new_dataframe = my_dataframe.merge(dataframe2, 
                                    how="<left, outer, inner, right>",
                                    left_on="column_name",
                                    right_on="column_name")
```


# read_csv
```python
my_dataframe = pandas.read_csv(my_csv_filepath)
```

##### See also
[read_excel](#read_excel)

# read_excel
```python
# returns dataframe of first sheet
my_dataframe = pandas.read_excel(my_xlsx_filepath)
```

```python
# returns dataframe of specified sheet
my_dataframe = pandas.read_excel(my_xlsx_filepath, sheet_name=['transition_temps','references'])
```

```python
# returns an ordered dict where each key is sheetname, each value is the associated dataframe
my_dataframes = pandas.read_excel(my_xlsx_filepath, sheet_name=['transition_temps','references'])
```

##### See also
[read_csv](#read_csv)

# shape
```python
(numRows, numCols) = my_dataframe.shape
```
