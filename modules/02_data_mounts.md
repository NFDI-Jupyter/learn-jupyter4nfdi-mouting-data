# Storage and mounts

Mounting does not necessarily mean copying all files from a remote system into Jupyter.
Instead, a storage system is made accessible at a particular location in the filesystem. That location is called a **mount point**.

Suppose remote storage contains:

```text
experiment-data/measurements.csv
```

It could appear inside your Jupyter environment as something like:

```text
data/experiment-data/measurements.csv
```

The important part is that the file may still physically live on another system.

Remember that mounting is not downloading, if you download a dataset, you make another copy. But if you mount storage, you make the remote location available to your Notebook. This distinction matters when datasets are large or when several people work with the same storage.

## Advantages of mounting storage

A mount can be useful when:

- the data is already stored somewhere else;
- you do not want duplicate copies;
- several people need to access the same data;
- the dataset is too large to copy unnecessarily.

