# Add

Let's go ahead and "stage" both the new file ("my-file.txt") and the changes to the README by running:

`git add README.md` (tab completion _should_ work)

`git add my-file.txt`

Now, let's run `git status` again.

Git reports that we have "Changes to be committed". These files are in a state called "staged" as in they are on the stage ready to be committed.

_NB: we did not have to explicitly add each file (adding hundreds of files would be extremely tedious). We can use a simple shortcut to add all changes: `git add .` where "." represents our current working directory._

# Reset

We can easily unstage changes (remove them from the staging area) or files by using the "reset" command on them. Let's unstage our changes to the README:

`git reset README.md`

It's important to note that `git add` and `git reset` are equal and opposite. Add stages the change/file and reset unstages it.

