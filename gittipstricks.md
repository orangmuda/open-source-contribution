# GIT TIPS AND TRICKS

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
git config --global alias.aadd .
git config --global alias.aliasesconfig --get-regexp alias
git config --global alias.alias! git config --get-regexp ^alias\\. | sed -e s/^alias.// -e s/\\ /\\ $(printf \"\\043\")--\\>\\ / | column -t -s $(printf \"\\043\") | sort -k 1
git config --global alias.apadd . -p
git config --global alias.addupsremote add upstream
git config --global alias.bdbranch -d
git config --global alias.bibisect
git config --global alias.blbranch -l
git config --global alias.blrbranch -a
git config --global alias.brbranch -r
git config --global alias.cacommit -a
git config --global alias.camcommit -a -m
git config --global alias.cicommit -m
git config --global alias.cmcommit
git config --global alias.cocheckout
git config --global alias.colastcheckout -
git config --global alias.commentscommit -m 📒Comments
git config --global alias.countrev-list --count
git config --global alias.dbbranch -D
git config --global alias.forgetAboutrm --cached
git config --global alias.formattingcommit -m 💅Formatting
git config --global alias.fpfetch -p
git config --global alias.grepgrep -F
git config --global alias.laffsck --lost-found
git config --global alias.lastlog -1 HEAD
git config --global alias.latestlog -5 --pretty --oneline
git config --global alias.lsls-files --others --exclude-standard -z
git config --global alias.mendcommit --amend
git config --global alias.nbcheckout -b
git config --global alias.opgc --prune=now --aggressive
git config --global alias.pfpush --force-with-lease
git config --global alias.popush origin
git config --global alias.poupush --set-upstream origin
git config --global alias.prpull --rebase
git config --global alias.prorremote prune origin
git config --global alias.prudpull --rebase upstream devel
git config --global alias.prumpull --rebase upstream master
git config --global alias.pruneremote update --prune
git config --global alias.ptagpush origin --tags
git config --global alias.rarebase --abort
git config --global alias.rcrebase --continue
git config --global alias.refactorcommit -m 👷Refactor
git config --global alias.remotesremote -v
git config --global alias.renbbranch -m
git config --global alias.rhreset --hard
git config --global alias.rhhreset --hard HEAD
git config --global alias.rirebase -i upstream/dev
git config --global alias.rlreflog
git config --global alias.sstatus -s
git config --global alias.searchrev-list --all
git config --global alias.shshow
git config --global alias.shortshortlog -sn
git config --global alias.signcommit --amend --signoff
git config --global alias.ststatus
git config --global alias.stashesstash list
git config --global alias.testscommit --allow empty -m ✅Tests
git config --global alias.unstashstash pop
git config --global alias.vcclean -dfx
git config --global alias.wowlog --all --graph --decorate --oneline --simplify-by-decoration
```

To easily display your git aliases run this command in your terminal - `! git config --get-regexp ^alias\. | sed -e s/^alias.// -e s/\ /\ $(printf "\043")--\>\ / | column -t -s $(printf "\043") | sort -k 1`.

Now you can use `git alias` to list all the aliases you have created.
