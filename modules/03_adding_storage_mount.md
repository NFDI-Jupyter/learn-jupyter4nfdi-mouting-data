# Adding an external storage mount

Jupyter4NFDI lets you configure external storage before starting JupyterLab. The exact fields depend on the storage system you select.

On the Jupyter4NFDI server configuration page:

1. Open the **Storage** tab.
2. Choose **Add Storage Mount**.
3. Select the storage type.
4. Enter the required configuration.
5. Choose where the storage should appear in your Jupyter environment.
6. Start JupyterLab.

You can configure more than one storage mount if your work requires it.

Possible configuration values include things such as:

```text
endpoint
bucket
username
password
access key
secret key
remote path
```

Not every storage type uses all of these. S3 and WebDAV, for example, use different connection information.

**Best practice**: Use clear mount names


```text
data
b2drop
project-data
shared-results
```

rather than:

```text
test123
new
stuff
```

This becomes more important once you have several mounts.

**Note**

Do not put any credentials for mounting data such as storage passwords, access keys or secret keys into notebooks or Git repositories!

