# Working with storage in Jupyter4NFDI

When working in Jupyter, you may have to use data which is stored somewhere else than your Notebooks. Due to the size of the data or licensing restrictions you may not be able to simply copy this data over. The data may be in: in B2DROP, an S3 bucket, a WebDAV server, or another storage service.

Jupyter4NFDI supports mounting external storage into a Jupyter environment. Once mounted, the files can be accessed much like other files available in JupyterLab.

## Learning objectives

After working through this material you should be able to:

- understand what mounting storage means;
- add an external storage mount;
- work with mounted files from JupyterLab, Python and the terminal;
- understand read-only and read-write access;
- document storage dependencies for reproducible work.

## Permanent storage

It is useful to distinguish between the **compute environment** and the **storage**. Jupyter4NFDI offers persistent storage. However, the lab (the image) you created isn't meant to be a permanent storage for all your work. Also, if you deleted the image from your dashboard, all files are gone. Therefore Jupyter4NFDI shouldn't be your main storage solution.

A solution is to have an external storage. Instead of first copying a dataset into Jupyter4NFDI, you can connect the Jupyter environment to the location where the data is already stored and then do your computational analysis.


**Thy this out:**

Start Jupyter4NFDI and open a terminal.

```bash
pwd
ls
```

Create a small file:

```bash
echo "storage test" > storage-test.txt
```

Open it from the JupyterLab file browser.

Think about which files should still be there after you stop and restart your Jupyter server.

