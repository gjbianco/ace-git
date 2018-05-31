# Conflicts

So, not all merges are so easy, unfortunately. When both the branch being merged into and the branch being merged from have changes to the same files _on the same lines_, we say that this merge has "conflicts". Git cannot automatically (like it normally does) merge the files. Human intervention must reconcile this situation.

We typically want to avoid situations where there are conflicts, but like any good Defense Against the Dark Arts, let's go ahead and practice that which should be avoided, so we are prepared when the situation arises.

First let's create a commit on our master branch. Edit the README.md file and be sure to change something *on the first line* of that file. It does not matter to what (but remember what it was). While on the master branch (`git checkout master`), stage and commit the file.

Now, let's switch back to our other branch by doing `git checkout my-branch`. Let's edit README.md again (note that your change on the other branch isn't there anymore!). Once again, be sure to edit *the first line* and go ahead and make it different from your other change. Now, once again add and commit the change.

Now, switch back to master yet again with `git checkout master`. Now start the merge with `git merge my-branch`.

Uh oh! We got a conflict! Git will put us in a special state until we either resolve the conflict or abort the merge (with `git merge --abort`). We want to resolve the conflict, though, as abort just puts us back where we were.

Open up README.md again. Now we see some special marker symbols ("<<<<<<", "=======", and ">>>>>>>") with each of our sets of changes in separate sections.

Your job is to make the file *how it should be* by changing it to one section, the other, both, neither, or something completely different. It is important to note that the marker symbols *should not be there* when you are finished (checking these symbols back into a repo is HUGE no-no) and, assuming the file is code (in this case, it is not), it should absolutely compile and *WORK*. Otherwise, our conflict resolution is not at all complete and we have failed to merge properly.

This should stress you a little. Fixing conflicts can be a daunting task sometimes, and that is exactly why we do what we can to avoid them where possible! A lot of new people to git get intimidated by the conflict resolution process. It is the most difficult part to overcome, but absolutely can be done so with practice, so fear not!

Let's continue. Get the README.md file in a good state following the above rules.

Check the state of our merge with `git status`. If we had other changed files that didn't have conflicts, we would see that they are already staged. However, since we only have the conflicted file, git has left it unstaged. So, with our fixed README.md, we have to tell git that we have fixed it by staging it with `git add README.md`.

Once all of our conflicted files are fixed and staged (we only had one so we are done), we can continue the merge with `git commit`. This will, as usual, drop us into the editor to provide a commit message. Since this is a special commit (a merge commit), git has created a basic message for us involving the branches involved and any conflict that arose. You can provide more information here, but I normally stick with the default one provided by git.

Once we save and quit the commit message, we are done! Merge complete! You can check that there is a new commit that git created with `git log`.

_NB: you may have noticed that the first merge does not have a commit of its own and it didn't even ask for a message! This is because git was able to do what is called a "fast-forward commit". We won't get into too much of the details here, but that basically means that the the branches did not diverge._
