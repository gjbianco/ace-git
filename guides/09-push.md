# Push

While we cannot easily demonstrate fetch or pull without others (please see the presentation for information on these), we can go ahead and use push.

Keep in mind that push is intended to push up to a repository. This includes any information in a commit and is not easily undone. Do not push any commits that contained information you do not want shared. Remember that git commits can be thought of as snapshots and, therefore, those snapshots can be easily restored by others.

With that in mind, let's go ahead and push our new branch to our GitHub repo.

First off, you will need to set up your own copy of the repo. Visit the repo's page at https://github.com/gjbianco/nch-example-repo

While logged in, go ahead and hit the "fork" button at the top right of the page. This will create a copy of the repo for your GitHub account. This fork of the project is your own copy, which means you automatically have push access to it. You can fork any public repositories to get your own copy (of the current state). Any new changes made by the original author are not automatically added to your repo, however.

Now that you have your fork, let's add it to the remote setup of our existing copy of the local repo.

Git remote allows you to set up multiple remote repositories. By default, since we cloned the project from elsewhere, it has already set that repository as "origin". You can view the URL of the origin repo by running:

`git remote show origin`

This also lists which branches are configured for push and pull. Notice that "my-branch" is not listed in any of those. We want to push our changes in my-branch to our repo.

Let's set up our new remote repo as a remote repo in git. Go to the page of your fork on the GitHub website. On the right hand side of the page, there is a "clone URL". Copy this URL (use the SSH version if you have keys set up, otherwise you'll have to use the HTTPS version). Now, back on the command line, add the remote with:

`git remote add fork <URL>`

Now run `git remote` and you'll see "fork" is now a remote that is set up. You can run `git remote show fork` to see the URL and any remote branches set up with that remote (this should only be master, currently).

Now, make sure you are on the branch "my-branch" (use `git checkout my-branch`). Now that we have our remote set up, we want to push the branch the new remote. If you were to run just `git push` right now, it would fail. The first time a new branch that you create locally is to be pushed, you have to set the "upstream" for that branch. To do this, you have to use the full version of the command and provide the `-u` option (for "[u]pstream"). Like so:

`git push -u fork my-branch`

This will push the changes to GitHub. Go ahead and visit the site and select the branch from the dropdown at the top left (you may need to refresh the page).

Back on the command line, go ahead and create some changes, then stage and commit them. These new commits are not in GitHub yet, so go ahead and push them with `git push`. Note that we did not need all of the same options this time since we already set our upstream.
