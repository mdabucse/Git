# Stashing Changes for Context Switching

## Overview
This task demonstrates how to use Git stash to temporarily save uncommitted changes, switch branches, and reapply the stashed changes.

## Steps Performed

1. **Make Changes Without Committing**
   - Modified `index.html` with temporary changes.

2. **Stash the Changes**
   - Used `git stash` to save the uncommitted changes.
   - Verified the working directory was clean using `git status`.

3. **Switch Branches and Perform Work**
   - Switched to a new branch `new-feature` and committed new work.

4. **Reapply Stashed Changes**
   - Switched back to the `master` branch and reapplied the stashed changes using `git stash pop`.

5. **View and Manage Multiple Stashes**
   - Used `git stash list` to view all stashes.
   - Applied a specific stash using `git stash apply stash@{n}`.
   - Dropped a stash using `git stash drop stash@{n}`.
   - Cleared all stashes using `git stash clear`.

## Repository Structure
```
Task-6/
    index.html
```