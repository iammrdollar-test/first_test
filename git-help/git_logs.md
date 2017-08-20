# Check GIT logs
  $ git log

# Check Reference Logs
  $ git reflog

-------------------------------------------------------------------------------

# Git log for a particular file
  $ git log -- FILENAME

## seeing the git log for the HEAD file
  $ git log -- HEAD

## seeing the git log for the HEAD reference
  $ git log HEAD --

## if there is no HEAD file you can use HEAD as commit reference
  $ git log HEAD

-------------------------------------------------------------------------------

# Check logs of head, head of head etc (~)
  $ git log HEAD~1
  $ git log HEAD~2

# Check logs of two heads of a merge (^)
  $ git log HEAD^1
  $ git log HEAD^2

# NOTE: The Git terminology is parent for ^ and ancestor for ~.


# Diff between logs of two different branches (double dot operator ..)
  $ git log branch1..branch2
  $ git log branch2..branch1

# The double dot operator allows you to select all commits 
# which are reachable from a commit c2 but not from commit c1. 
# The syntax for this is "c1..c2"
# A commit A is reachable from another commit B if A is a direct or indirect parent of B.
# Think of c1..c2 as all commits as of c1 (not including c1) until commit c2.

# e.g. See new commits made locally
  $ git log origin..master

-------------------------------------------------------------------------------

# Triple Dot Operator (...)
# The triple dot operator allows you to select all commits which are
# reachable either from commit c1 or commit c2 but not from both of them.
# This is useful to show all commits in two branches which have not yet been combined.

> show all commits which
> can be reached by master or testing
> but not both
  $ git log master...testing

-------------------------------------------------------------------------------

# Check a particular author's log

  $ git log --author="<part-of-name>"
