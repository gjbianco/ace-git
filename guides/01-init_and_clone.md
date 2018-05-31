# Init and Clone

The `git init` command is pretty straightforward. Let's go ahead and create a new repository by running (run this outside of an existing git repository such as the NCH repo; a good alternative is just your Desktop directory):

`git init my-project`

This will create a new directory called "my-project" that has a ".git" directory underneath it. This is where git stores all of its files. Removing this directory will leave the other files, but remove git tracking (so be careful!).

The other way you can get a git repo to play around with is by cloning one. Go ahead and clone the example one (also outside of any git repos) by running this command:

`git clone git@github.com:gjbianco/nch-example-repo.git`

or, alternatively, if you don't have SSH keys set up in GitHub

`git clone https://github.com/gjbianco/nch-example-repo.git`
