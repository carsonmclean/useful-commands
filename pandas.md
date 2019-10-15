# Pandas
## Print more rows/columns

```python
pd.set_option('display.max_rows', 100)  # If exceeded, truncated with ... (depending on display.min_rows)
pd.set_option('display.max_columns', 10)  # If exceeded, truncated with ...
pd.set_option('display.width', 200) # If width of rows exceeds display.width, columns are wrapped around underneath (until display.max_rows is reached)

# Alternative syntax (equivalent to above)
pd.options.display.max_rows = 0  # Setting to zero takes the current width of the terminal (often 80)
```
https://pandas.pydata.org/pandas-docs/stable/user_guide/options.html
