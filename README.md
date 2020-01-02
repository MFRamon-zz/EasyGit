# Easy Git


## Objective :
> The main purpose of this list of git commands is to help other open source contributors to get started with the usage of git. Some of these commands have helped me solve some of the problems 
that I have encountered while learning git.

## Managing multiple git credentials:
> Say you want to be using multiple git accounts.Managing multiple git accounts usin OSX can be a little bit of a burden if you're trying to pull & push through HTTPS protocol as you have to be erasing the credentials that OSX stores in its built in keychaing application every time you need to interact with your remotes. so for that the best option is to authenticate each Github account with an SSH key.

Though if you wanna be interacting with git through HTTPS protocol,you could do that by erasing your credentials every time you want to change the commit's author and email.

In order to reset the credentials that OSX stores in its keychain application you need to do the following :

```sh
$ git credential-osxkeychain erase
host=github.com
protocol=https
<press return>
```
After this,the next time you try to interact with your remote,git will prompt you to set you Git username and email.
Configuring an SSH Key for each of your accounts would be done as following : 

TODO: To add process of configuring account using SSH

This is a basic workflow on how to start a git repo : 

Inside your projects root directoy add a README.md file that explains a little bit about what the repo is about:

# Create that file in Terminal by doing

```sh
# Create a README.md with the most important information
$ touch <file_name>

# Create .git subdirectory to start the new repo
$ git init

# OPTIONAL : Verify if the URL for pushing and fetching is already set otherwise set it :
$ git remote add <remote_name> <repo_url>
 
# After having it added just verify it was set correctly
$ git remote show <remote_name>

# If push/fetch URLS are set,you're ready to start doing by doing the next workflow
$ git add <path_to_file_for_commit>

# Save your commit
$ git commit -m "<commit_message"
```
You are ready to push to your remote branches by doing : 

$ git push origin 

If you haven't linked you local branch to a remote tracking branch the push won't work so for that you'll need to add the reference to the branch you want to push in your remote

$ git push -u <renote_name> <remote_tracking_branch>


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
$ git push <remote> -d <bramch_name>

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

git reset --hard old_sha1
git push --force upstream master:master
```
