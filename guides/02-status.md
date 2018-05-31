# Status

The `git status` command is probably the most used command in all of git. This command simply reports back the current state of affairs according to git. This command will list if you have untracked changes, untracked files, staged changes/files, or even unpushed or unmerged commits (when dealing with remotes).

Go ahead and create a file called "my-file.txt" in the nch-example-repo (you can just run `touch my-file.txt` in Linux).

Now run `git status`

Git should tell you that you have an untracked file. This means that git has never seen this file before.

Now edit "README.md" (e.g. you can use vim or nano). Be sure to actually make a change.

Now run `git status` again. Notice how git mentions "README.md", but it is listed under _untracked changes_. Git recognizes the file, but sees that you have made changes to it.

