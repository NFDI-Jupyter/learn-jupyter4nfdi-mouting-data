# Troubleshooting and common issues

Some of the common issues you may encouter are:

1. The mounted directory is empty. 
 Possible reasons:
    - you entered the wrong path;
    - the credentials you entered do not give you access to the data files/folders;
    - the configuration doesn't match the storage service;
    - the remote location actually doesn't contain files.

2. I can read files but cannot create files
 Possible reasons: 
    - the mount may be read-only (and this may be by design).  Before changing the configuration, ask whether write access is actually needed.

3. Python says the file does not exist
 Possible reasons:
    - check if you are working in the right directory (relative to the data path).

    ```python
    from pathlib import Path
    print(Path.cwd())
    ```

4. The data loads slowly from the external storage.
    Possible reasons:
    - slow network (this may be temporary);

    Things that may help:

    - avoid repeatedly reading the same large file;
    - avoid unnecessary scans over thousands of tiny files;
    - process only the subset you need;
    - consider whether a temporary local working copy is appropriate for your workflow.

5. The credentials do not work.
  Possible reasons:
    - you made a mistake in configuration steps, check the documentation.

Different systems may expect different kinds of credentials, for example:

- username and password;
- application password;
- token;
- access key and secret key.

