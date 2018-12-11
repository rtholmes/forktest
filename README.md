# magical repo syncing

### Main repos:

* `ubccpsc/classy/master` (hereby `root`) is the stable source for the repo
* `<user>/classy/master` (hereby `fork`) is where classes are going to want to work (there will be many of these `fork` repos)

### Goals:

* `fork/master` needs be able to make any changes it needs during the term without impacting `root/master`
* `fork/master` needs to be able to accept critical patches during the term from `root/master`
* `fork/master` needs be able to accept new feature changes at the end of the term
* `fork/master` needs to be able to contribute changes to `root/master`

#### Fork initialization

1. fork `root` into an account you control
1. create a branch called `sync` on your `fork`
1. add the upstream branch `git remote add upstream https://github.com/ubccpsc/classy.git` ([LINK](https://help.github.com/articles/configuring-a-remote-for-a-fork/))


