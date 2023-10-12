# The Regular Workflow.

In an ideal world, you want to keep both your remote repositories in sync. However, your current changes only exist on the `internal` repository and not the `startup` repository. How do you get these changes over to the latter without messing up production?

The first thing you must understand is that you will only sync the repositories once your PRs have been merged into the `dev` branch of the `internal` repository.

The second thing you must understand is that you will sync these changes by pushing the `dev` branch of the `internal` repositories as a new branch to the `startup` repository, thus enabling you to create a PR on the `startup` repository too.

So practically, you are dealing with two PRs, one on the `internal` repository and the other on the `startup` repository.
When the `internal` one gets merged, it is a green signal for you to push those changes to the `startup` repository.

Additionally, you will come across situations where you need to resolve merge conflicts, but the strategy listed in these guides tries to minimize the number of times you need to resolve them - in most cases, you only need to resolve them when pushing changes to the `startup` repository, if at all.

Now, to understand the process itself, consider the cases you may come across when you show up to work on the next working day.

---

### Case 1: Internal Merged, Not Pushed to Startup.

To tackle this case, read [case-one](cases/case-one.md).

---

### CASE 2: Internal Merged, Created on Startup, Not Merged on Startup.

To tackle this case, read [case-two](cases/case-two.md).

---

### CASE 3: Merged on Both Repositories.

To tackle this case, read [case-three](cases/case-three.md).

---

### CASE 4: Internal Not Merged, Requires Edits.

To tackle this case, read [case-four](cases/case-four.md).

---

### CASE 5: Internal Not Merged, Reviewer Busy.

To tackle this case, read [case-five](cases/case-five.md).
