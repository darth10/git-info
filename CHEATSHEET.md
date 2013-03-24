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

TODO

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
* Use the `--rebase` option to perform a rebase instead of a merge.

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

TODO

## Extras

TODO
