# magical repo syncing

### Main repos:

* `ubccpsc/classy/master` (hereby `root`) is the stable source for the repo
* `<user>/classy/master` (hereby `fork`) is where classes are going to want to work (there will be many of these `fork` repos)

### Goals:

* `fork/master` needs be able to make any changes it needs during the term without impacting `root/master`
* `fork/master` needs to be able to accept critical patches during the term from `root/master`
* `fork/master` needs be able to accept new feature changes at the end of the term, but only a ***subset*** of commits
* `fork/master` needs to be able to contribute changes to `root/master`

#### Fork initialization

1. fork `root` into an account you control
1. create a branch called `sync` on your `fork`
1. add the upstream branch `git remote add upstream https://github.com/ubccpsc/classy.git` ([LINK](https://help.github.com/articles/configuring-a-remote-for-a-fork/))

#### Development process

* Do all your `fork` work on `fork/master` or other branches, just not on `fork/sync`.

##### Pulling changes from `root/master` into `fork/master` 

This can happen regulairly, whenever there is a `root/master` change that fixes a bug or adds a feature that the fork might want.
 
On `fork`:
1. `git checkout master`
1. `git fetch upstream` (pulls down the changes)
1. `git merge upstream/master` (merges them into master)
1. `git push`

##### Pushing changes from `fork` to `root/master`

This is ***not*** likely to happen during the term, except for critical patches but it _is_ likely to happen at the end of the term when new features should be upstreamed to `root`.

