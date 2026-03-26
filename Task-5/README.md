# Interactive Rebasing for Clean Commit History

## Overview
This task demonstrates how to use interactive rebasing to clean up commit history by squashing, reordering, and editing commit messages.

Interactive rebasing allows you to modify your commit history. You can:
- Reorder commits: Change the order of commits.
- Edit commits: Modify the content or message of a commit.
- Squash commits: Combine multiple commits into one.

## Steps Performed

1. **Create a Series of Commits**
   - Made three commits with minor changes and typos in commit messages.

2. **Run Interactive Rebase**
   - Used `git rebase -i HEAD~3` to start an interactive rebase for the last 3 commits.
   - Squashed the commits into a single commit and edited the commit message of the squashed commit.

3. **Modify Commit Messages**
   - Used the `reword` option to edit/change the commit messages:
     1. Start the rebase: `git rebase -i HEAD~3`.
     2. Replace `pick` with `reword` for the desired commit(s).
     3. Save and close the editor to proceed.
     4. Edit the commit message(s) as prompted and save.

4. **Remove Unnecessary Commits**
   - Used the `drop` option to eliminate redundant or irrelevant commits:
     1. Start the rebase: `git rebase -i HEAD~3`.
     2. Replace `pick` with `drop` for the commit(s) to be removed.
     3. Save and close the editor to apply the changes.

5. **Fix Commit Content**
   - Used the `edit` option to amend the content of a specific commit:
     1. Start the rebase: `git rebase -i HEAD~3`.
     2. Replace `pick` with `edit` for the commit to be modified.
     3. Save and close the editor to pause the rebase.
     4. Make the necessary changes to the files.
     5. Stage the changes: `git add <file>`.
     6. Amend the commit: `git commit --amend`.
     7. Continue the rebase: `git rebase --continue`.

6. **Verify the Rebase**
   - Verified the commit history using `git log --oneline`.

## Repository Structure
```
Task-5/
    index.html
```