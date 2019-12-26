# git-list-commands


This is a short list of git version control.


## Objective :
> The main purpose of this list of git commands is to help other open source contributors to get started with the usage of git. Some of these commands have helped me solve some of the problems 
that I have encountered while learning git.


```sh
# Switch between branches
$ git checkout <branch_name>

# Merge a remote branch into the one you're currently at
$ git merge origin/<branch_name>

# Deletes a local branch if you have already pushed it & merged it to a remote branch
# -d stands for --delete 
$ git branch -d <branch_name>

# Force a delition of a local branch
# -D stands for --delete --force
$ git branch -D <branch_name>

#List only the remote branches
# git branch -r

#List all the local & remote branches
# git branch -a
```
