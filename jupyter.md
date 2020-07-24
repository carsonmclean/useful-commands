# Jupyter
## Expand Cell to Fill Browser Window
```python
from IPython.core.display import display, HTML
display(HTML("<style>.container { width:90% !important; }</style>"))
```

## Print floats with decimals instead of scientific notation
```python
pd.set_option('display.float_format', lambda x: '%.3f' % x)
```
