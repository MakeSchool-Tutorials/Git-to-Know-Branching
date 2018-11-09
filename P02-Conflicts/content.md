---
title: "Coping with Conflicts"
slug: conflicts
---

Let's practice what to do when your branch doesn't merge flawlessly with `master`.

# Step 1: Creating a Conflict Script

In order to explore merge conflicts, we'll need to generate one in your repository!

> [action]
> Create a new file in the root of the repository named `make-conflict.sh`, and ensure it can run using the `chmod` utility.
>
```bash
$ touch make-conflict.sh
$ chmod +x make-conflict.sh
```
>

> [action]
> Paste the following code inside `make-conflict.sh` and save the file.
>
```bash
touch my_code.sh
git add my_code.sh
echo "echo Hello" > my_code.sh
git commit -am 'initial'
git checkout -b new_branch
echo "echo \"Hello World\"" > my_code.sh
git commit -am 'first commit on new_branch'
git checkout master
echo "echo \"Hello World!\"" > my_code.sh
git commit -am 'second commit on master'
git merge new_branch
```
>

> [action]
> Run the script using the command below. Examine the last two lines of output. What happened?
>
```bash
$ ./make-conflict.sh
>
[master (root-commit) cc780d8] initial
 1 file changed, 1 insertion(+)
 create mode 100644 my_code.sh
Switched to a new branch 'new_branch'
[new_branch 3cb9aa2] first commit on new_branch
 1 file changed, 1 insertion(+), 1 deletion(-)
Switched to branch 'master'
[master 20700cb] second commit on master
 1 file changed, 1 insertion(+), 1 deletion(-)
Auto-merging my_code.sh
CONFLICT (content): Merge conflict in my_code.sh
Automatic merge failed; fix conflicts and then commit the result.
```
>

Git wasn't able to merge the changeset automatically!

It needs your help in order to rectify the changeset.

Next, let's learn how to inform Git about the changes we want to keep, and the changes we want to discard.

# Step 2: Viewing the Conflict

> [action]
> To see the beginning of the merge conflict in your file, open `my_code.sh` in your editor and search the file for the conflict marker `<<<<<<<`.
>
```bash
<<<<<<< HEAD
echo "Hello World!"
=======
echo "Hello World"
>>>>>>> new_branch
```
>

When you open the file in your text editor, you'll see the changes from the HEAD or base branch after the line `<<<<<<< HEAD`.

Next, you'll see `=======`, which divides your changes from the changes in the other branch, followed by `>>>>>>> new_branch`, the branch we attempted to merge into `master`.

# Step 3: Merge Manually

> [action]
> Decide if you want to keep only your branch's changes, keep only the other branch's changes, or make a brand new change, which may incorporate changes from both branches.
>
> Delete the conflict markers `<<<<<<<`, `=======`, `>>>>>>>` and make the changes you want in the final merge.
>
> In this example, both changes are incorporated into the final merge.
>
> Here's what the `my_code.sh` file looks like in it's final form:
>
```bash
Hello World
```
>

# Acheivement Unlocked: Mega Merge Master

**Way to level up your Git skills --- you're ready to handle branches, merges, and conflicts in your day-to-day projects!**
