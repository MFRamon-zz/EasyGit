# Easy Git


## Objective :
> The main purpose of this list of git commands is to help other open source contributors to get started with the usage of git. Some of these commands have helped me solve some of the problems 
that I have encountered while learning git.


```sh
# Use it to set your own Git email to a local repository
$ git config user.email "<email>"

# Use it to set your own Git username to a local repository
$ git config user.name "<username>"

# Show the current configuration for your git repository such as the Fetch / Push URL, remote and local branches
$ git remote show <remote>

# Show the remote tracking branch for each of the branches
$ git branch -vv

# Create and checkout to a new branch
$ git checkout -b <new_branch_name>

# Set the track remote branch on your remote associated with the your local branch
$ git push -u <remote> <remote_branch>

# Switch between branches
$ git checkout <branch_name>

# Merge a remote branch into the one you're currently at
$ git merge <remote>/<branch_name>

# Deletes a local branch if you have already pushed it & merged it to a remote branch
# -d stands for --delete 
$ git branch -d <branch_name>

# Delete a remote branch 
# git push <remote> -d <bramch_name>

# Force a delition of a local branch
# -D stands for --delete --force
$ git branch -D <branch_name>

# List only the remote branches
$ git branch -r

# List all the local branches
$ git branch -l

# List all the local & remote branches
$ git branch -a

# How to rename a local branch
$ git branch -m <old_branch_name> <new_branch_name>

# Delete all stale references from the upstream branches so they can be updated on your local
$ git remote update —prune

# Reset a single file from you modified files list
$ git checkout -- <path_to_file>

# Stash the local changes in your working directory providing a description message with it
$ git stash save "<stash_message>"

# List all the stashes you have stored locally
$ git stash list

# Remove a stash from the list given its identifier
$ git stash drop <stash_item_identifier>

# Apply a stash given its identifier onto your working tree but still kepp it your stash
$ git stash apply <stash_item_indentifier>

# 

```
