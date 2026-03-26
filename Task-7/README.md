# Cherry-Picking Commits Between Branches

## Overview
This task demonstrates how to selectively apply a commit from one branch to another using Git's cherry-pick feature.

## Steps Performed

1. **Initialize the Repository**
   - Ran `git init` to initialize a new Git repository.

2. **Create and Commit Changes in `master`**
   - Created `index.html` and made an initial commit.
   - Made another commit with updated content.

3. **Create and Commit Changes in `feature-branch`**
   - Created a new branch `feature-branch`.
   - Modified `index.html` and committed the changes.

4. **Cherry-Pick a Commit**
   - Identified the commit hash from `feature-branch` using:
     ```sh
     git log feature-branch --oneline
     ```
   - Cherry-picked the commit into `master` using:
     ```sh
     git cherry-pick <commit-hash>
     ```

5. **Handle Conflicts**
   - Resolved conflicts manually in `index.html` (if any).
   - Continued the cherry-pick process using:
     ```sh
     git cherry-pick --continue
     ```

6. **Verify the Commit History**
   - Verified the commit history using:
     ```sh
     git log --oneline
     ```

## Repository Structure
```
Task-7/
    index.html
```