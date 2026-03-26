# Simulating and Resolving Merge Conflicts

## Overview
This task demonstrates how to simulate and resolve merge conflicts in Git by modifying the same file in two branches.

## Steps Performed

1. **Create a Repository and a Common File**
   - Initialized a Git repository and created `index.html` with initial content.

2. **Create Two Branches**
   - Created `branch-a` and modified the `<h1>` tag.
   - Created `branch-b` and modified the same `<h1>` tag.

3. **Simulate a Merge Conflict**
   - Merged `branch-a` into `master`.
   - Merged `branch-b` into `master`, causing a conflict.

4. **Resolve the Conflict**
   - Manually resolved the conflict in `index.html` by combining changes.
   - Marked the conflict as resolved and committed the merge.

5. **Verify the Merge**
   - Verified the commit history and file content to ensure the conflict was resolved.

## Key Commands Used
- `git merge <branch>`: Merge a branch into the current branch.
- `git status`: Check the status of the repository.
- `git diff`: View differences between conflicting changes.

## Repository Structure
```
Task-4/
    index.html
```