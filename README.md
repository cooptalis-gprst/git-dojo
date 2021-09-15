# git rebase --interactive 🕑

This is where you learn to actually rewrite history in git :) With this command, you can for instance:

- **edit** commits
- change the **name** of commits
- change the **order** of commits
- **discard** commits
- and much more

You basically become a wizard 🧙‍♂️

The **only command you can use** is:

```bash
git rebase -i HEAD~<N> # (e.g. git rebase -i HEAD~4)
```

You can also commit and force-push changes.

**Please read carefully git output**. git is quite verbose when you're doing an interactive rebase, and gives you some valuable hints about what are the steps you should follow.

**You will also probably need to change git default editor**; otherwise, depending on your operating system (I'm looking at you, MacOS), you might end up using Vim, which might not be ideal. To do so, execute the following:

- `git config --global core.editor nano` if you want to use nano as your editor of choice
- `git config --global core.editor "code --wait"` if you want git to use VS Code

## First exercise

Some files are already committed, with their name as content. Unfortunately, it appears some files have some weird content in it. You must fix them so that every file only contains their name (e.g. `file-1` must contain "file-1", `file-2` must contain "file-2", and so on). **The commit history must stay unchanged**, i.e. must look like this:

1. README for `git rebase -i`
1. Add file-1
1. Add file-2
1. Add file-3
1. Add file-4
1. Add file-5

## Second exercise

You actually **don't want files with an odd number**. How would you make your commit history look like this?

1. README for `git rebase -i`
1. Add file-2
1. Add file-4

Your working directory **must not contain files that are not committed**; file-1, file-3 and file-5 must not be in your working directory. They must be *gone* ✨

## Third exercise

You want to give fancier names to your commits, like this:

1. docs(README): write instructions for `git rebase -i`
1. feat(files): add the second file
1. feat(files): add the fourth file

Remember that the only command you can use, is `git rebase -i` 😉

## Fourth exercise

You want to **change the order of your commits**, so that your commit history looks like this:

1. docs(README): init instructions for `git rebase -i`
1. feat(files): add the fourth file
1. feat(files): add the second file
