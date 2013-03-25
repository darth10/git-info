## Initial setup

* Set your commit author user name and email, using something like `git config --global user.name 'Akhil Wali'` and `git config --global user.email 'akhil.wali.10@gmail.com'`.

## Creating 

* Create a git repository using `git init`.
* Use the `--bare` option to make it a bare repository, which can serve as a remote.
* Cloning a remote repository also creates a new local repository.

## Committing

* Add files using `git add`. Add everything in the current directory using `git add .`.
* Remove files using `git rm`.
* Commit using `git commit`. Set `$GIT_EDITOR` to your favorite editor.
 
![commits](http://git-scm.com/figures/18333fig0310-tn.png)

* Add everything and commit using `-a` option. Use carefully.
* Ammend last commit using `--amend` option. Very useful.

## Reverting

* Revert all changes in a file using `git checkout FILE`.
* Revert a commit by creating a new commit using `git revert COMMIT`. Useful when you've pushed bad commits.
* Revert a commit without creating a new commit using `git reset HEAD~NO_OF_COMMITS`. Useful when you have bad commits that are not yet pushed.
* Use the `--hard` option with `git reset` to checkout the file as well. Use carefully.
* To undo all changes in your working tree, use `git reset --hard HEAD`.

## Cloning

* Clone a repository using `git clone URL`.

![clone](http://git-scm.com/figures/18333fig0322-tn.png)

## Syncing

### Push

* Push using `git push REMOTE BRANCH`.
* Use the `-f ` option to force overwriting the remote repository. Of course, you should have write permissions.
* Use the `-a` option to push all branches.
* Use the `--tags` option to push tags.

### Pull

* A `git pull REMOTE BRANCH` is equivalent to a `git fetch ORIGIN BRANCH:NEW_BRANCH`, followed by a `git merge NEW_BRANCH`. 

![fetch](http://git-scm.com/figures/18333fig0324-tn.png)

* The `NEW_BRANCH` branch is actually named `ORIG_HEAD`.

## Branching and Rebasing

* List all branches using `git branch`. Use the `-a` option to include remote branches.
* Create a new branch using `git checkout -b NEW_BRANCH`.

![branch](http://git-scm.com/figures/18333fig0327-tn.png)

* Merge commits into your current branch using `git merge BRANCH_TO_MERGE`.
* Fast-forwards by default. Use the `--no-ff` option to skip fast-forward.
* Use the `--no-commit` option with the `--no-ff` option to skip commit. Very useful.

![merge](http://git-scm.com/figures/18333fig0328-tn.png)

* Rebase your current branch on another branch using `git rebase REBASE_BRANCH`.
* Use the `-i` option to perform a special rebase called an *interactive* rebase. One of the coolest features of git.

![rebase](http://git-scm.com/figures/18333fig0329-tn.png)

* Rebasing is encouraged as the person merging your commits can fast-forward. Thus, lesser redundant commits and a cleaner history.

![ff-merge](http://git-scm.com/figures/18333fig0330-tn.png)

## Conflicts

* When you have conflicts, it means you better rebase our work, or else more people will run into conlicts. Of course, your work should be a separate branch if you have to rebase.
* If a file as conflicts, use the `--theirs` or `--mine` option with `git checkout` to resolve conflicts. You can also do this manually.
* Make sure you mark the file as resolved using `git add FILE`.
* If you're performing a merge, commit the changes. If you're performing a rebase, continue the rebase using `git rebase --continue`.
