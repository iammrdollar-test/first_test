





# Git Add & Commit
> git add and commit at the same time (only modified and deleted files)
> NOTE: No untracked files are added

  $ git commit -am "Message"


# Git Pull
> git pull fetches contents from remote repo to local and shows conflicts if any

  $ git pull

> NOTE: git pull is equal to "git fetch" and "git merge"

# Cross-Check with remote repo
> Show what would be done, without making any changes.

  $ git fetch --dry-run

# Reset to a previous version (git reset)
> Go back to some previous point in repo

  $ git reset --hard <commit-hash>

> Now commit it and push (--force to overcome Fast-Forward Error Message)

  $ git commit -m "Message for resetting"
  $ git push --force

> If you added some files and made some changes and thought at everthing is 
> messed up and want to go back to the original copy at remote, do
  
  $ git reset --hard origin/master

> NOTE: use "git reset --soft <hash>" to soft reset, meaning it will not remove
>       any file, but will add them to the staging area
> NOTE: use "git reset <hash>" to do reset and show what's resetted, but will 
>       remove any file. It will untrack the files.
