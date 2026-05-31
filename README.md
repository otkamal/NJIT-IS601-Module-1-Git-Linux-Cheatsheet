# IS601 Linux and GIT Cheatsheet

This document serves as a reference sheet to useful commands used on Linux systems and the GIT versioning control system.

## Linux

Navigate the Linux CLI
```{bash}
# show current directory
pwd

# show contents of current directory
# -l = list contents, -a = all content (includes hidden files)
ls -la

# move to another directory
cd <directory-name>
```

Basic file interactions.
```{bash}
# create an empty text file
touch <filename>

# delete a file
rm <filename>

# rename a file
mv <old-name> <new-name>

# move a file to a new location
mv <old-location> <new-location>

# copy a file to another location
cp <file> <new-location>

```

Basic directory interactions.
```{bash}
# create a new directory
mkdir <new-directory>

# delete an empty directory
rmdir <directory>

# delete a directory and all of its contents
rm -rf <directory>

```

Basic process interactions
```{bash}
# view running processes
top

# get PID for specific process
pgrep <string-to-search>

# end process gracefully
kill <pid>

# force terminate process
kill -9 <pid>

```

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

View branches and create a new one
```{bash}
# view all branches
git branch

# create a new branch
git branch <new-branch-name>

# alternatively `git switch -c` can be used as a shortcut to git branch and git checkout
git switch -c <new-branch-name>
```

Merge changes from one branch into the current branch
```{bash}
# checkout the branch to merge changes into
git switch <branch-to-merge-changes-into>

# merge changes from the changed branch into the current branch
git merge <branch-to-merge-changes-from>
```

Pull (or pull and merge) remote branches to a local repository
```{bash}
# just grab remote branches 
git fetch <remote-alias>

# e.g.
git fetch origin

# grab remote branches and automatically merge commits into local branches
git pull
```

Push a local branch upstream to remote Git repository.
```{bash}
git push <remote-alias> <local-branch>

# e.g.
git push origin ok/my-new-branch
```
---
