# Comprehensive Workflow with Forced Pushes and Recovery

## Overview
This task demonstrates an advanced Git workflow involving forced pushes, recovering lost commits, and managing a multi-branch workflow.

## Steps Performed

1. **Set Up the Repository**
   - Initialized a Git repository and linked it to a remote.

2. **Created Multiple Branches**
   - Created `feature-branch` and `bugfix-branch` with distinct changes.
   - Pushed both branches to the remote.

3. **Simulated a Forced Push**
   - Rewrote history on `feature-branch` using an interactive rebase.
   - Performed a forced push to update the remote branch.

4. **Recovered Lost Commits**
   - Used `git reflog` to locate and recover a lost commit after a mistaken force push.
   - Created a new branch (`recovered-branch`) to restore the lost commit.

5. **Merged Branches**
   - Merged `feature-branch` and `bugfix-branch` into `main` and pushed the changes to the remote.

## Repository Structure
```
Task-10/
    index.html
```