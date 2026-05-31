# IS601 Linux and GIT Cheatsheet

This document serves as a reference sheet to useful commands used on Linux systems and the GIT versioning control system.

## Linux
---

## GIT

Initialize a local directory as a Git directory.

```{bash}
git init <directory>
```

Pull a remote repository from a hosted location. Depending on the method of authentication, the format of the specification of the remote repo can vary.

```{bash}
git clone <remote-repository>

# e.g. with SSH auth
git clone git@github.com:otkamal/mod1_cheatsheet.git
```

Show the status of files in the local directory

```{bash}
git status
```
---
