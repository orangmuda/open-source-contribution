# GIT TIPS AND TRICKS 🔥🚀⚡

For Git basics visit this link - [Git basics](https://rogerdudler.github.io/git-guide/).

A repo containing only Git tips and tricks.

**`git log -10 --pretty --oneline`**

Displays your last 10 latest commits, each on their line.

`-10` can be replaced with any number you want.

**`git checkout -`**

Jumps back to your last branch.

**`git reflog`**

Displays all the steps you have made

**`git log -s mykeyword`**

Searches through your commits for a commit matching your keyword.

Replace `mykeyword` with the word you want to find

**`git switch -c "new_branch"`**

Did you make the changes in the wrong branch?

This command creates a new branch and moves all your changes to the newly created branch.

**`git switch "branch_name`**

The same as above, but it moves the changes to an existing branch.

**`git log --graph --oneline --decorate --all`**

An ASCII art tree of all the branches, decorated with the names of tags and branches.

**`git commit --amend`**

Edit the **last commit message** and save the commit. If you have already pushed the code, push again by using `--force` flag to make changes to remote repository.

**`git shortlog`**

Summarizes git log output in a format suitable for inclusion in release
announcements. Each commit will be grouped by author and title. ([source](https://git-scm.com/docs/git-shortlog)) ([@natterstefan](https://twitter.com/natterstefan/status/1244888942165610497))

## GIT ALIASES

Create shorter git commands with git aliases.

To add new ones, use the following command `git config --global alias.[insertYourShortcut] [gitCommand]`.

These are mine:

```bash
git config --global alias.a add .
git config --global alias.aliases config --get-regexp alias
git config --global alias.alias ! git config --get-regexp ^alias\. | sed -e s/^alias.// -e s/\ /\ $(printf "\043")git config --global --\>\ / | column -t -s $(printf "\043") | sort -k 1
git config --global alias.ap add . -p
git config --global alias.addups remote add upstream
git config --global alias.bd branch -d
git config --global alias.bi bisect
git config --global alias.bl branch -l
git config --global alias.blr branch -a
git config --global alias.br branch -r
git config --global alias.ca commit -a
git config --global alias.cam commit -a -m
git config --global alias.ci commit -m
git config --global alias.cm commit
git config --global alias.co checkout
git config --global alias.colast checkout -
git config --global alias.comments commit -m 📒Comments
git config --global alias.db branch -D
git config --global alias.forgetabout rm --cached
git config --global alias.formatting commit -m 💅Formatting
git config --global alias.fp fetch -p
git config --global alias.laf fsck --lost-found
git config --global alias.last log -1 HEAD
git config --global alias.latest log -5 --pretty --oneline
git config --global alias.mend commit --amend
git config --global alias.nb checkout -b
git config --global alias.pf push --force-with-lease
git config --global alias.po push origin
git config --global alias.pou push --set-upstream origin
git config --global alias.pr pull --rebase
git config --global alias.pror remote prune origin
git config --global alias.prum pull --rebase upstream masgit config --globalter
git config --global alias.prune remote update --prune
git config --global alias.ra rebase --abort
git config --global alias.rc rebase --continue
git config --global alias.refactor commit -m 👷Refactor
git config --global alias.remotes remote -v
git config --global alias.renb branch -m
git config --global alias.rh reset --hard
git config --global alias.rhh reset --hard HEAD
git config --global alias.ri rebase -i upstream/dev
git config --global alias.rl reflog
git config --global alias.s status -s
git config --global alias.short shortlog -sn
git config --global alias.stashes stash list
git config --global alias.tests commit -m ✅Tests
git config --global alias.unstash stash pop
git config --global alias.vc clean -dfx
git config --global alias.wow log --all --graph --decorate --oneline --simplify-by-decoration
```

To easily display your git aliases run this command in your terminal - `! git config --get-regexp ^alias\. | sed -e s/^alias.// -e s/\ /\ $(printf "\043")--\>\ / | column -t -s $(printf "\043") | sort -k 1`.

Now you can use `git alias` to list all the aliases you have created.
