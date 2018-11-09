---
title: "Get Branching with Git"
slug: branching
---

> **If you ever talk to a great programmer, you'll find they know their tools like an artist knows their paintbrushes.**
>
> -Bill Gates

This tutorial details a step-by-step strategy to enhance your development workflow called **git branching**. Branching is often referred to as the "killer feature" of Git.

## Command Overview

The commands we'll be running in each step are listed below for your future reference. Save it in your notes!

> [solution]
>
```bash
$ cd ~/dev/repos/
$ git clone git@github.com:droxey/git-branchy.git
$ cd git-branchy
$ git pull origin master
$ git checkout -b develop master
$ git add .
$ git commit -m "[add] code from step 5 of sweet git tutorial"
$ git pull origin master
$ git push origin develop
$ git checkout master
$ git pull origin master
$ git merge develop
```
>

## Purpose of Branching

Successful teams follow **three rules to integrate git into their daily workflow**:

1. **Commit early and often.**
1. **Don't break master.**
    * The code in `origin/master` **always** works.
    * **No errors**, no UI glitches.
    * **No exceptions**.
1. **Use branches.** A branch can represent:
    * A brand new **feature**.
    * **Bug fixes**.
    * Works **in progress**.
    * Individual contributions **that aren't ready to be deployed**.

Sold? Let's try it out! Follow the step-by-step guide below to create and push your own branch to GitHub!

# Step 1 - Create a New GitHub Repository

> [action]
> First, create a [new GitHub repository](https://github.com/new) to serve as a playground for this tutorial.

# Step 2 - Create a Local Clone

> [action]
> On your **local** machine, `cd` to the project directory. In git, this is known as your **working directory**, which was created when you executed `git clone` at the beginning of the project.
>
```bash
$ cd ~/dev/repos
$ git clone git@github.com:droxey/git-branchy.git
>
Cloning into 'git-branchy'...
remote: Enumerating objects: 233, done.
remote: Counting objects: 100% (233/233), done.
remote: Compressing objects: 100% (158/158), done.
remote: Total 233 (delta 120), reused 173 (delta 62), pack-reused 0
Receiving objects: 100% (233/233), 35.28 KiB | 5.04 MiB/s, done.
Resolving deltas: 100% (120/120), done.
```

# Step 3 - Pull Updates Early and Often

> [action]
> Update your **local** repository with the latest revision of `origin/master`.
>
```bash
$ git pull origin master
>
remote: Counting objects: 6, done.
remote: Total 6 (delta 2), reused 2 (delta 2), pack-reused 4
Unpacking objects: 100% (6/6), done.
From ssh://github.com/droxey/git-branchy
branch            master     -> FETCH_HEAD
383e9d7..7766d57  master     -> origin/master
Updating 383e9d7..7766d57
Fast-forward
README.md | 25 ++++++++++++++++++-------
1 file changed, 18 insertions(+), 7 deletions(-)
```
>

# Step 4 - Creating a Branch

Now that your **local** `master` branch is up-to-date with your team's latest changes, create a branch locally by **running the exact command** below. There are other ways to do this, but **this one is foolproof**.

The syntax below creates a new branch named `develop` based on an existing branch, `master`.

> [action]
> Run the following command to create the `develop` branch locally:
>
```bash
$ git checkout -b develop master
```
>

# Step 5 - Generate a Changeset

Write that fancy new feature, fix that bug, experiment; it's showtime!

> [action]
> Create a new file. Add some code. We trust you --- you've been doing this a while! For example, I added a file named `test.js` to my directory.
>
> Once complete, run the following commands to add and commit your changeset to your local repository.
>
```bash
$ git add .
$ git commit -m "[add] code from step 5 of sweet git tutorial"
```
>

# Step 6 - Integrate Upstream Changes

> [action]
> Integrate upstream changes from `origin/master`, which adds them to our **local** branch.
>
```bash
$ git pull origin master
>
From ssh://github.com/droxey/git-branchy
 * branch            master     -> FETCH_HEAD
Already up-to-date.
```
>

# Step 7 - Push Your New Branch

> [action]
> Push your new branch, as well as your changeset, to `origin/develop`.

```bash
$ git push origin develop
>
Counting objects: 16, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (16/16), done.
Writing objects: 100% (16/16), 1.49 KiB | 1.49 MiB/s, done.
Total 16 (delta 14), reused 0 (delta 0)
remote: Resolving deltas: 100% (14/14), completed with 14 local objects.
To ssh://github.com/droxey/git-branchy.git
[new branch]      'develop' -> 'develop'
```
>

This branch is now available on your `origin` – simply open up GitHub (or GitLab, Heroku, Bitbucket, etc) to verify! When complete, it's a good idea to ask a friend or colleague to review your code.

Once your code is bug-free and release-ready, merge it to the `master` branch.

> [info]
> Repeat this process each time you finish a part of the feature or need to take a break. Branches are considered works in progress – so commit and push to your branche(s) as much as possible; **even if it's not done**! If something goes terribly wrong, `origin/develop` serves as a history, backup, and record of your valuable work!

# Next Step

Ready for primetime? Proceed to the next page to learn how to merge your code into the `origin/master` branch on GitHub.
