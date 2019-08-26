# Printing Info
## Print to file and console
```python3
import sys

class Tee(object):
    def __init__(self, *files):
        self.files = files
    def write(self, obj):
        for f in self.files:
            f.write(obj)
            f.flush() # If you want the output to be visible immediately
    def flush(self) :
        for f in self.files:
            f.flush()

f = open('out.txt', 'w')
original = sys.stdout
sys.stdout = Tee(sys.stdout, f)

# CODE HERE

sys.stdout = original
f.close()
```
https://stackoverflow.com/questions/11325019/how-to-output-to-the-console-and-file
