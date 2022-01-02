# Cheatsheet - Git commands

### General info 

```
1. You can use different git remote hosts that allows you to store your git repositories:
A. Github - Free public Repositories. Paid Private Repositpres

B. Bitbucket - By default, your code repositories are private. Free for individuals & Small teams with up to 5 users, with unlimited public and private repositories.

```

> To get free Bitbucket account - press [here](https://bitbucket.org/product/)

> To sign-in to your exiting Bitbucket account - press [here](https://bitbucket.org/account/signup/)

> To install Git - press [here](https://www.atlassian.com/git/tutorials/install-git)


### First time Git setup

```
# Configure your username
git config --global user.name "<name>"

# Change username
git config --global --replace-all user.name "<name>"

# Configure your user email
git config --global user.email "<email>"

# Set default editor you'll like to use for Git
git config --system core.editor <editor>

## i.e ##
git config --system core.editor "'C:\Program Files\Notepad++\notepad++.exe'"
git config --system core.editor nano

# Output the current configuration
git config --list
```


### Initializing Repository in a directory

```
# Initailizing a Git directory
git init        ##Git will store all of your git information on the '.git' directory
```


### Adding remote origin

```
# Copy your repo's URL and specify your git remote origin 
git remote add origin https://bitbucket.org/MW_1991/demo/src/master/

# To check which remote origin on our directory has already configured for
git remote -v
```

### Branches Introduction

> When you create a brach, you must always start from another branch

> Usually, main/master branch is the latest stable code branch that the developers will have to create their branch from it and will merge their branch to it

> There are scenarios, which there is a possible to get a branch conflict. If there are different branches with the same file names, same lines on a file, etc.


For more details of Git branches, press [here]()


### Tracking remote branches

```
# To check what currently branch we are on right now and all of the local branches
git branch -a      ## Shows a list of your local branches. Use -v flag instead, for verbose mode

# Fetch code to local branch from remote branch
git fetch origin <branch_name>

# Merge code to local branch from remote branch
git merge origin <branch_name>

# Fetch & merge code to local branch from remote branch
git pull origin <branch_name>

# Check the status of the local git
git status

# Add all of your new changes files to prepare for commit (for remote branch)
git add .

# Verify you've ready to commit all of your changes
git status

# Enter a commit message to show after push the changes to the remote branch
git commit -m "Describe here your changes"

# Push your commit to the remote branch
git push origin <branch_name>

## Fot the first push, use the --force flag  
git push origin --force <branch_name>       ## --foce = -f
```

### Creating & Pushing branches

```
# To create a local new branch and to change your local branch to it
git checkout -b <new_branch_name> <existing_branch_name_to_clone_from>

# Switch between local branches
git checkout <existing_branch_name>

# After commiting the <new_branch_name> changes, push this new branch to the remote repository by setting an upstream branch
git push --set-upstream origin <new_branch_name>
```


### Fetching Changes

```
# Fetch all the changes from the remote branch
git fetch --all     ## Fetch a 'creaed-online branch for example'

# Output a list of your remote branches
git branch -r       ## List all remote branches
```


### Deleting Branches

```
# Use the --delete flag and delete from your remote origin a specific branch
git push -d origin <remote/local_branch_name> ## the 'created-online' for example

# Same, but delete only locally
git branch -D <remote/local_branch_name>
```

### Merging & Conflicts

> When there's a merge conflicts, you can check where are they pressing cntrl+f (find option) on your IDE and search for the value of '<<<<<<< HEAD'

> Then, Press your chosen option (Accept Current Change / Accept Incoming Change / Accept both changes)

> Finally, after you've done, commit your changes and push to the remote branch


### Revert Bad commit

> When you have committed a bad commit and you want to revert it, you need to use its commit-id

```
# To get the commit id
git log --oneline

# git revert <commit_id>    ### After that, choose your commit (of revert) message
```

### Git stash
> We can store our work in the stash if we want to go to another branch before committing our changes, and return to our changes (restore the changes after we go back to the same branch we've started those changes)

```
# Store our changes
git stash save

# To see our stash items
git stash list

# Restore our last changes from the stash
git stash apply

# To clear your stash
git stash clear
```



## Resources
> [AHT Cloud Youtube link](https://youtu.be/1tC6Z57AOkY)

> [Atlassian official documentation](https://wac-cdn.atlassian.com/dam/jcr:e7e22f25-bba2-4ef1-a197-53f46b6df4a5/SWTM-2088_Atlassian-Git-Cheatsheet.pdf?cdnVersion=140) (Downloads the official PDF cheatsheet)