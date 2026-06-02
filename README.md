# IS601 Linux and Git Cheatsheet

Cheatsheat for basic Linux and Git operations.

## Linux

### Navigate the CLI
```{bash}
pwd                     # show current directory
ls -la <directory-path> # show contents of directory (including hidden files)
cd <directory-name>     # move to another directory
```

### File interactions
```{bash}
touch <filename>                    # create an empty text file
rm <filename>                       # delete a file
mv <old-name> <new-name>            # rename a file
mv <old-location> <new-location>    # move a file to a new location
cp <file> <new-location>            # copy a file to another location
```

### Directory interactions
```{bash}
mkdir <new-directory>   # create a new directory
rmdir <directory>       # delete an empty directory
rm -rf <directory>      # delete a directory and all of its contents
```

### Process interactions
```{bash}
top                         # view running processes
pgrep <string-to-search>    # get PID for specific process
kill <pid>                  # end process gracefully
kill -9 <pid>               # force terminate process
```

### Text operations
```{bash}
cat <path-to-file>                           # display contents of a file
grep <search-string> <path-to-file>          # search for string in file
sed 's/<find>/<replace>/g' <path-to-file>    # find and replace string in file

```
---
## Git

### Set things up
```{bash}
git init <directory>            # initialize a local directory as a Git directory.
git clone <remote-repository>   # pull a remote repository and contents to local directory
```

### Create branches
```{bash}
git branch                      # view all branches
git branch <new-branch-name>    # create a new branch
git switch -c <new-branch-name> # create a new branch and switch to it
```
> [Conventional branching](https://conventionalbranch.org/) for writing good branch names.

### Evaluate changes
```{bash}
git status          # show the status of files in the local directory
git diff            # to compare unstaged changes against branch
git diff --staged   # to compare staged changes against branch
```

### Make changes
```{bash}
# STEP 1
git add .                       # stage all files in directory
git add <file(s)>               # stage specific file

# STEP 2
git commit -m <commit message>  # commit staged changes
```
> [Conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) for writing good commit messages.

### Merge changes
```{bash}
git merge <branch-to-merge-changes-from> # merge changes from the changed branch into the current branch
```

### Push/Pull Changes
```{bash}
git fetch <remote-alias>    # fetch remote branches, but don't merge
git pull                    # fetch remote branches, and merge them

git push <remote-alias> <local-branch> # push a local branch upstream to remote Git repository.
```