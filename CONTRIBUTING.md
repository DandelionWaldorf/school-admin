# How to contribute to this repository

- The `master` branch should always be in a deployable state. It is deployed automatically on staging environment on
  each new commit.

- [We are not following GitFlow](https://www.endoflineblog.com/gitflow-considered-harmful), there is no `dev` branch.

- All work is done in short lived feature branches that are merged to `master` once they have been tested and approved.

- Commit history is kept linear.

In order to keep our commit history linear and easy to navigate, we're following a few simple rules:

- Only [fast-forward merges](http://ariya.ofilabs.com/2013/09/fast-forward-git-merge.html) are allowed. Gitlab's repo
  has already been set up for this so only `Rebase and Merge` button is available for all PRs. Alternatively you can
  merge PRs from command line:
  ```
  git fetch origin                    # fetch latest changes from Github
  git rebase -i origin/master         # rebase your branch on top of master and squash multiple commits
  git push -f origin <my_branch>      # update the remote branch on Github
  git push origin <my_branch>:master  # push your branch as master. This will succeed only if your branch
                                      # is rebased on top of master and if the PR has been approved.
                                      # It also merges the PR and deletes the feature branch on Github.
  ```

- Before merge ensure commits are [squashed](http://gitready.com/advanced/2009/02/10/squashing-commits-with-rebase.html):

  1. Each commit should be well-tested product increment
  2. PR should usually have only one commit
  3. Multiple commits per PR are acceptable in rare cases when each commit is a complete work unit.

- [Write meaningful commit messages](https://chris.beams.io/posts/git-commit/), prefix it with ticket number in square
  brackets
