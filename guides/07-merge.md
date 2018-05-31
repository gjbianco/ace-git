# Merge

Merging branches, in most cases, is pretty easy. Let's go ahead and create a couple of changes on our "my-branch" branch by editing the README.md and committing the change (remember to stage the change first). Go ahead and create another file with some random contents and commit it *in a separate commit* (you will need to stage and add twice, providing two separate commit messages).

Now we can do a merge. The basic idea is that the merge command will merge the branch that we provide *into* our current branch. Since we want to merge our new commits into master, first we have to switch to the master branch by doing:

`git checkout master`

Now we can actually merge our new branch into master by doing:

`git merge my-branch`

This takes all of the _commits_ that we made on our "my-branch" branch and puts them in master. Note that the changes have to be committed in order for them to be merged!

If we run `git status` we see that we are on master, and if we run `git log` we see that our two new commits are here on master now, too.
