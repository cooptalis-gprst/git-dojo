# git dojo 🥋

Welcome to the git dojo! The goal of this dojo is for you to master some common day-to-day git commands, such as:
- `git reset HEAD~<N>`
- `git commit --amend`
- `git rebase --interactive`

Each set of command exercises has its own branch, namely:
- `git-reset-head`
- `git-commit-amend`
- `git-rebase-i`

**Do note** that this tutorial is supposed to be done ***exclusively from the command line***. No graphical tool is allowed.

## Setup

Fork the project from the command line:

1. in GitHub (or whichever git hosting service of choice), create a new project named « git-dojo »
1. `git clone https://github.com/cooptalis-gprst/git-dojo`
1. `cd git-dojo`
1. `git remote set-url upstream https://github.com/cooptalist-gprst/git-dojo`
1. `git remote set-url origin https://github.com/<your_username>/git-dojo`

Note that if you have an SSH key set up on GitHub, you could (and should) replace `https://github.com/<your_username>/git-dojo` with `git@github.com:<your_username>/git-dojo`.

Once done, you can checkout to the dojo branches with the following commands:

```bash
git checkout --track upstream/<branch_name> # e.g. git checkout --track upstream/git-reset-head
git push --set-upstream origin <branch_name> # e.g. git push --set-upstream origin git-reset-head
```

Instructions will be in the README :)

## Useful command: take a peek at your commit history

To have a quick peek at your commit history, `git log` would come in handy, but is quite verbose. If you want to display your commit history in a more compact way, with only the SHA of your commits followed by their names, you can use the `--oneline` option, like so:

```bash
git log --oneline
```

If you want only to see the last three commits, you cant use:

```bash
git log --oneline -3
```

As the command is quite long, you can set up a ✨git alias✨

```bash
git config --global alias.lo "log --oneline" # You can replace alias.lo by alias.unicorn or whatever
```

Then, you would only need to type:

```bash
git lo -3 # Or: git unicorn -3
```
