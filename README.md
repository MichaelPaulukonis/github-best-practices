adapted from https://github.com/skyscreamer/yoga/wiki/GitHub-Best-Practices



Here are some suggested practices for how to contribute to a project.

## A. Set Up
Make sure you have an account on github: http://help.github.com/mac-set-up-git/ or http://help.github.com/win-set-up-git/

## B. Create your own fork
Go to the project home and click on the fork button to create your own fork.
http://help.github.com/images/bootcamp/bootcamp_3_fork.jpg

## C. Clone the fork locally
    % git clone git@github.com:<username>/<reponame>.git

## D. Add your contributions
It is a git best practice to develop each new feature or bug fix in a new branch, and we strongly recommend you do the same with descriptive branch names.  It's trivial to create branches and switch between them.  Using them will make it simple for you to pause one task list item and begin another.  It also simplifies our process of tracking contributions to the main code base.  Submitting pull requests for the same branch over and again can sometimes lead to unexpected results, so the basic process should be:

### 1. Checkout a new branch
    % cd <reponame>
    % git checkout -b my_descriptive_branch_name

You'll immediately be in the new branch.  Remember this isn't Subversion or CVS, so the branch checkout doesn't create a new directory, it changes the state of your working directory, adding/removing files as necessary to update the state.

### 2. Implement your changes
If you are using an IDE, now is when you'll want to refresh (Eclipse) or Git->Synchronize (IntelliJ) to make sure your editor is in sync with the git repo on your filesystem.

Now, write some code!

### 3. Stage and commit your changes
Git requires files be staged before committing.  You can add the files manually:

    % git add <file>

Or add the **-a** tag when you commit.

When you commit, just do the following:

    % git commit

This will commit your changes to your local copy of the repository (which is _distinct_ from your fork on github).

### 4. (Optional) Merge down the primary code base

If you know changes have been made to the primary code base, or if a pull request has been denied because you are out of sync with the primary code repository, you'll need to do a merge.

First create a "remote" to the primary (aka upstream) code repository.  You only need to do this once ever.  You're basically defining an alias that can be reused across checkouts:

    % git remote add upstream git://github.com/<username>/<reponame>.git

Retrieve and merge updates:

    % git fetch upstream
    % git merge upstream/master

### 5. Push your changes

    % git push origin my_descriptive_branch_name

If you cloned from another source than your fork, you can create a remote to your fork, and push to that fork instead of origin.

### 6. Submit a pull request

Go to your fork on the web site (e.g. http://github.com/<username>/<reponame>), and click on the "Pull Request" button on the top.  Under the base branch you should see **skyscreamer/yoga @ master** and under the head branch **_username_/yoga @ master**.  Replace "master" in the head branch with the name of your new branch (e.g. my_descriptive_branch_name).  Press enter, and click the "Update Commit Range" at the bottom.

You should then be able to add a descriptive comment about what is in this merge, and submit the pull request.  A project admin can then apply the merge to the primary code repository.

You can read more about pull requests here: http://help.github.com/pull-requests/

## E. Rinse and repeat

## More Reading

A helpful guide to previewing submitted pull requests is here: http://beust.com/weblog/2010/09/15/a-quick-guide-to-pull-requests/

For more reading, check out the excellent Pro Git book online, especially the Public Small Project section in chapter 5.2: http://progit.org/book/ch5-2.html.  Also check out github's "Fork a Repo" help page: http://help.github.com/fork-a-repo/

mvn jetty:run-war
