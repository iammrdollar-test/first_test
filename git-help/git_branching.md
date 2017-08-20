# Show Git Branches

> Current branch is marked with * 

  $ git branch

> Show remote branches

  $ git branch -r

> Show all Git Branches (Local + Remote)
  $ git branch -a


# Create a new git branch

  $ git branch <new-branch-name>


# Move/Checkout to a branch

  $ git checkout <branch> 

> NOTE: Use "git checkout -b <new-branch>" to create a branch 
>       and checkout at the same time


# Push the branch to github

  $ git push origin <branh-name>


# Update branch from remote
> Update your branch when the original branch from official repository has been updated

  $ git fetch <name-of-your-remote>

# Set default branch for git push

  $ git push --set-upstream origin <branch-name>
or
  $ git push -u origin <branch-name>


# Merge two branches
> Merges given branch with the current branch you are on.

  $ git merge <branch-name>

> To merge to your parent branch (form the branch you branched)
> Then you need to apply to merge changes,
> if your branch is derivated from develop you need to do :

  $ git merge <name-of-your-remote>/develop


# Delete the merged branch

> This will delete git branch locally

  $ git branch -D <branch-name>

> To delete git branch from remote repo, use

  $ git branch origin :<branch-name>

> NOTE: The only difference is the : to say delete.


# Add a new remote for your branch :

  $ git remote add <name-of-your-remote>

# Push changes from your commit into your branch :

  $ git push <name-of-your-new-remote> <name-of-your-branch>
