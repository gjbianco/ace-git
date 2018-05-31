# Commit

While `git status` might be the most used command in git, but `git commit` is probably the most important. As you should have seen in the presentation, committing is so important that *it is both a noun and a verb*.

Let's try creating a commit!

In order to create a commit, we have to have changes. Well, we actually already have those! Namely, our new file called "my-file.txt" and our changes to "README.md" (follow the steps in the previous Labs, if you haven't already).

So, now we have our changes. It is important to note that *git _only_ commits changes that are staged*. To demonstrate this, let's first look the state of our repo with `git status`.

We see that the new file ("my-file.txt") is staged, but the changes to our README *are not*.

Let's go ahead and commit the staged change with `git commit`.

At this point, a text editor should show up (either what is set to $EDITOR or vim). Git is prompting you for a "commit messae". As you should have read in the presentation, commit messages are extremely important. So important that, if you do not provide one, git assumes that you want to cancel the commit process altogether.

So, since we want to continue with the commit, let's provide it a commit message. It does not matter what this message is, so go ahead and write whatever you want.

_NB: if you do not have an editor set and you are not familiar with vim, you can just press the 'i' key to enter INSERT mode, type your message, press the 'Escape' key, then type ":wq" without quotes (this will save the changes and quit vim in one command)._

Run `git status` to see that our only remaining change is our change to README.md (since that wasn't staged when we ran commit), but our "my-file.txt" is still there.

Go ahead and stage the changes to the README.md and commit the change (providing a useful commit message). Run `git log` again to see the new commit.
