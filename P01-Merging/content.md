---
title: "Merging to Master"
slug: merging
---

# Step 1: Move to Master Branch

> [action]
> In your local repository directory, run the following command to switch to the `master` branch.
>
```bash
$ git checkout master
>
Switched to branch 'master'
```
>

# Step 2: Pull the Latest Changes

> [action]
> Pull the latest changes from `origin/master`, integrating the changesets into your local repository.
>
```bash
$ git pull origin master
>
From github.com:droxey/git-branchy
* branch            master     -> FETCH_HEAD
Already up to date.
```
>

# Step 3: Merge!

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

# Step 3: Success

We've practiced what to do in successful merge scenarios. Awesome! But what happens when things go awry? Follow the next step of the tutorial to practice how to deal with merge conflicts!