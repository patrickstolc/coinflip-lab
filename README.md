# Coinflip Lab: End-to-end Algorithmic Trading using Machine Learning

Coinflip Lab is a library for **algorithmic trading** in Python. The library is built for research as well as production. The development of the library is done iteratively and based on research conducted on https://coinflip.so.

Coinflip comes with data covering everything from market price data to social media sentiment data. Data processing in the library is based on Pandas and Numpy.

# Install Coinflip using pip
Using pip, Coinflip releases are available as source packages and binary wheels. Before installing Coinflip and its dependencies, ensure that your pip, setuptools, and wheel are updated.
```bash
pip install -U pip setuptools wheel
pip install coinflip-lab
```

# Usage
For more usage examples, please check out the notebooks [here](https://github.com/patrickstolc/coinflip/tree/main/examples).

## Universe
### Loading Dataset
```python
from coinflip.universe import load

df = load('AAPL', 'reddit_mentions')
df.head()
```

### Removing Dataset
```python
from coinflip.universe import remove

remove('AAPL', 'reddit_mentions')
```

### Fusing Datasets
```python
from coinflip.universe import fuse

df = fuse([('AAPL', 'ticks'), ('AAPL', 'fundamentals')])
df.head()
```
