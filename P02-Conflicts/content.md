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
> Run the script using the command below. What happens?
>
```bash
$ ./make-conflict.sh
```
>

# Step 2: Become a Merge Master

`#TODO`

# Ready for More?

Want to learn more? The final page of this tutorial includes some handy resources to dive deeper.
