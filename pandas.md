# Pandas
## Print more rows/columns

```python
# Automatic (set at begininning of file/near imports)
pd.options.display.width = 0

# Manual
pd.set_option('display.max_rows', 500)
pd.set_option('display.max_columns', 500)
pd.set_option('display.width', 1000)
```
https://stackoverflow.com/a/11711637
