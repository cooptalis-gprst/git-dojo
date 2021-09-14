# git reset HEAD~ 🤯

This command is to **untie recent commits**, back from the **Nth last commit** up to **HEAD**.

The **only commands you can use** are:

- `git reset HEAD~`
- `git reset HEAD~ --hard`
- `git reset HEAD~<N>` (e.g. `git reset HEAD~3`)
- `git rm <file>` (e.g. `git rm README.md`)

You can also commit and force-push changes.

Read along for instructions.

## First exercise

Some files are already committed. Unfortunately, you want to only keep files with an **even number in their name**. How would you do it?

By the end of this step, the commit history should be:

1. README for `git reset HEAD~<N>`
1. Add files with an even number in their name

The last commit should not contain any file with an odd number in their name, and your working directory shouldn't contain any odd number file.

## Second exercise

You now want to have one commit for each separate file. How would you do that?

By the end of this step, the commit history should be:

1. README for `git reset HEAD~<N>`
1. Add file-2
1. Add file-4
1. Add file-6
1. Add file-8
1. Add file-10

## Third exercise

You don't want file-10 anymore. How would you make your commit history look like this?

1. README for `git reset HEAD~<N>`
1. Add file-2
1. Add file-4
1. Add file-6
1. Add file-8

file-10 should **not be in your working directory anymore**.

## Fourth exercise

You finally want to have files which number is a **multiple of 4**. How would you make it possible?

By the end of this step, your commit history should be:

1. README for `git reset HEAD~<N>`
1. Add file-4
1. Add file-8

Your working directory should **not contain any other file** than the ones committed.
