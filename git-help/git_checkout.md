# git checkout - Switch branches and restore working tree files

> Updates files in the working tree to match the version in the index or
> the specified tree. If no paths are given, git checkout will also update
> HEAD to set the specified branch as the current branch.

# Switch to a different branch

  $ git checkout <branch>

> To prepare for working on <branch>, switch to it by updating the index and 
> the files in the working tree, and by pointing HEAD at the branch.
> Local modifications to the files in the working tree are kept, 
> so that they can be committed to the <branch>.

  $ git checkout -b <branch>

> Creates and checks out branch at the same time.

# Revert a file

  $ git checkout -- filename.txt

> This command reverts the filename.txt to the last commit you made.


The following sequence checks out the master branch, reverts the
           Makefile to two revisions back, deletes hello.c by mistake, and gets
           it back from the index.

  $ git checkout master             (1)
  $ git checkout master~2 Makefile  (2)
  $ rm -f hello.c
  $ git checkout hello.c            (3)
 
