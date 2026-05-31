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

Compare the difference of unstaged and staged files against previous commit.

```{bash}
# to compare unstaged changes
git diff

# to compare staged changes
git diff --staged
```

Add file to staging.
```{bash}
git add <file(s)>

# e.g.
# add all files in directory
git add .

# add just README.md
git add README.md
```

Commit staged changes. [This](https://www.conventionalcommits.org/en/v1.0.0/) is a good resource for writing good commit messages.
```{bash}
git commit -m <commit message>

# e.g.
git commit -m "fix(README): adjusted punctuation" 
```
---
