---
title: "Merging to Main"
slug: merging
---

> **Talk is cheap, show me the code!**
>
> -Linus Torvalds

Ready to merge to `origin/main`?

Let's make it happen using the following three step process!

# Step 1 - Move to Main Branch

> [action]
> In your local repository directory, run the following command to switch to the `main` branch.
>
```bash
$ git checkout main
>
Switched to branch 'main'
```
>

# Step 2 - Pull the Latest Changes

> [action]
> Pull the latest changes from `origin/main`, integrating the changesets into your local repository.
>
```bash
$ git pull origin main
>
From github.com:YOUR_USERNAME/git-branchy
* branch            main     -> FETCH_HEAD
Already up to date.
```
>

# Step 3 - Merge!

> [action]
> Let's merge by running the command below!
>
```bash
$ git merge develop
>
Merge made by the 'recursive' strategy.
test.js              |  0
1 files changed, 1 insertions(+), 0 deletions(-)
create mode 100644 test.js
```
>

# Step 4 - Push to GitHub

> [action]
> Add or stage your changes, commit them, and push them to GitHub.
>
```bash
$ git add .
$ git commit -m "[add] merge the develop branch"
$ git push origin main
```
>

# Next Step

We've practiced what to do in successful merge scenarios. Awesome! But what happens when things go awry? Follow the next step of the tutorial to practice how to deal with merge conflicts!
