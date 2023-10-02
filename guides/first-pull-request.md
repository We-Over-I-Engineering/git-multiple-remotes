# First Pull Request.

Once you have configured both the remotes on your `local` repository and have the codebase replicated between them, you can move on to create your first PR on the `internal` repository.

If there are multiple developers working on a project, I recommend that you create one PR each and not more to get started. This will help each of you to understand the workflow and sync your changes to the `startup` repository at least once before things get a little more complicated.

I also recommend that one PR is merged at a time. This will allow the developer to pull their changes from the `internal` repository and push them to the `startup` repository themselves the first time. Later on, this flow can change subject to communication within the team.

---

### STEP 1: Create a branch.

Before you make any changes to accomplish a task, you must switch to the `dev` branch and create a new one from there for your task. The following commands switch to `dev`, creates a new branch named `feature/auth-otp`, and switches to the newly created branch to start coding.

```
git switch dev
git branch feature/auth-otp
git switch feature/auth-otp
```

---

### STEP 2: Stage and commit changes.

Say that it took you some two hours to make your changes and you want to commit these changes now. You can do so normally with the help of the following commands.

```
git add .
git commit -m "<message-here>"
```

---

### STEP 3: Push changes.

When you push changes, you must push them to your `internal` repository only.

```
git push internal feature/auth-otp
```

Then, you must create a PR from `feature/auth-otp` to `dev` from the GUI, add some reviewers and ask them to merge the changes when satisfied. To keep things clean and simple, switch back to `dev` and delete `feature/auth-otp` from your `working directory`.

```
git branch -d feature/auth-otp
```

If the command above throws an error, use `-D` instead.

```
git branch -D feature/auth-otp
```
