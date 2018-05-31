# Branch / Checkout

While the presentation will explain more about the _why_ of the commands, let's go through the basic steps of creating a branch and traversing them.

You can see your list of branches as well as which one you are on by running `git branch` with no other arguments.

To create a new branch _off of your current branch_ (in our case, master), you can give the branch an argument:

`git branch my-branch`

This will only create a new branch called "my-branch". Note that this does not change our current branch (i.e. we are still on master).

To change to the new branch, we have to use the "checkout" command. Do this now by running:

`git checkout my-branch`

We are now on the "my-branch" branch. _NB: `git status` will also tell you which branch you are currently on._

Also, if we wanted to both create a new branch off of our current one AND switch to it in one command, we can provide the `-b` option to the checkout command. For example, *instead* of doing the above two steps, we could have simply done:

`git checkout -b my-branch` (doing this now will fail since the branch already exists)
