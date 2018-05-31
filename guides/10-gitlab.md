# GitLab

It is important to note that GitHub and git, while similar, are fundamentally different. One can use git without GitHub. However, since GitHub has historically (and for good reason) been very closely tied to the git community. It provides great tools for teams to collaborate and better organize, host, and discover code.

One of the most useful features that GitHub provides is the concept of "Pull Requests". For a GitHub repository, only people that have been given explicit "push access" are able to commit code back into the repository (even open source projects that allow anybody to download the code don't let anybody other than a trusted few push back to the repo). This whitelist does not lend itself well to projects that are intended to have hundreds or even thousands of committers. Especially when some of those committers might only need to contribute a single patch or feature to a repo.

Enter Pull Requests. They allow repository owners to maintain control over what code gets into their repo while still providing a way for people to contribute back to the project.

The basic process of creating a Pull Request is:

1. Clone the project to your own GitHub account (some projects do not do this step or even officially allow clones; if you are not sure, ask)
2. Create a new branch with a useful and unique name for your feature/fix (often, issue tracking numbers should be included in this name)
3. Make the changes and commit them to your branch.
4. Be sure to push the branch back to GitHub. (Note that, although your code is in GitHub, it is _not_ yet back into the main branch of the project)
5. Create a Pull Request from your branch in your project to the target branch of the target repository (note that this does not have to be the same repository as yours and often is not)
  - This can be done by viewing the branch on GitHub (using the autocomplete dropdown towards the top left of the page) and selecting "Create Pull Request".

  Once a Pull Request is created, it will show up in a special section where the project reviewers (trusted people given push access that can merge or decline pull requests) can view the proposed code changes, add comments, and either merge the pull request (bringing it into the project) or deny it (closing the request and decline the merge, at least for the time being).

  Generally, it is good practice to "commit early, commit often". Since git keeps track of the full history of code, it is easy to revert back to a previous state. Once untracked code changes are gone, though, they are gone forever (they are untracked!). For these reasons, it is good to commit code as you progress through making the changes, even if they are not finished. As long as what you eventually merge back into master (either directly or through a Pull Request) works and is generally stable.











Now that you have your commits pushed to a branch in GitHub, visit that branches page again (using the dropdown). Now, go ahead and create a pull request back to the original project (the gjbianco version) by selecting the green button (the tooltip will mention creating a pull request).

This is actually just the "Compare changes" page. You are comparing the differences of two different branches. At this point, you are sort of "previewing" what changes would be included in a pull request were you to make one.

Make sure your base is set to your copy of the "my-branch" branch. Now, go ahead and select "compare across forks" since we want to create a pull request back to the original copy of the project. Leave the base fork as yours, but change the head fork to the gjbianco version and select the compare branch to be master. This is telling GitHub (_not_ git) that you want to create pull request from your repo's copy of the branch "my-branch" _into_ the gjbianco version of the branch called "master".

Hit "Create pull request", fill out the rest, and submit.
