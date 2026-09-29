# Storage and reproducible research

There are some considerations around reproducibility when using external storage. If somebody runs your notebook later, will they know where the data came from and how it should be mounted? For example, if you mounted external data source and your code includes:

```python
df = pd.read_csv("/mnt/project/my-data.csv")
```

The notebook alone does not explain:

- which storage service `/mnt/project` refers to;
- which dataset version was used;
- who has access;
- whether the dataset may change;
- how the storage should be mounted.

At a minimum include metadata about your data in the README, including information about the data storage and its provenance (if relevant).

## Data paths 

Avoid hardcoding the data path across the code in your notebook. A better practice is to use one variable (it may also be referred to as a constant):

```python
from pathlib import Path

DATA_DIR = Path("data/raw")
df = pd.read_csv(DATA_DIR / "my-data.csv")
```

