# Undoing Changes and Reverting Commits

## Overview
This task demonstrates how to undo changes in the working directory and safely revert or reset commits.
## Steps Performed

1. **Undo Changes using `git restore`**
  - Created a new file named `index.html` and added initial content.
  - Commit the file and added some changes.
  - Used `git restore` to undo the changes:
    ```sh
    git restore index.html
    ```
2. **Undo Changes using `git checkout`**
  - Alternatively, also used `git checkout --` to undo the changes:
    ```sh
    git checkout -- index.html
    ```
  - Verified the changes were undone using:
    ```sh
    git status
    ```

3. **Undo a Commit Using `git revert`**
  - Made a new commit named "Added changes in index.html[ADD]"
  - Reverted the last commit using:
    ```sh
    git revert HEAD
    ```
  - Verified that a new commit was created to undo the changes:
    ```sh
    git log --oneline
    ```

4. **Undo a Commit Using `git reset`**
  - Reset the repository to the previous commit:
    ```sh
    git reset --soft HEAD~1
    ```
  - Verified the commit history to see the branch pointer moved back:
    ```sh
    git log --oneline
    ```

## Repository Structure
```
Task-3/
    index.html
```
## Comparison of Git Commands for Undoing Changes

| Command            | Purpose                                                                 | Scope                          | Creates New Commit | Usage Example                     |
|--------------------|-------------------------------------------------------------------------|--------------------------------|--------------------|------------------------------------|
| `git restore`      | Undo changes in the working directory or staging area                  | File-level                    | No                 | `git restore index.html`          |
| `git checkout`     | Undo changes in the working directory (deprecated for this purpose)    | File-level                    | No                 | `git checkout -- index.html`      |
| `git revert`       | Revert a specific commit by creating a new commit                      | Commit-level                  | Yes                | `git revert HEAD`                 |
| `git reset --soft` | Move the branch pointer to a previous commit, `keeping changes staged`   | Commit-level                  | No                 | `git reset --soft HEAD~1`         |
| `git reset --mixed(default)`| Move the branch pointer to a previous commit, `keeping changes unstaged`. `Keeps changes in working directory` | Commit-level                  | No                 | `git reset --mixed HEAD~1`        |
| `git reset --hard` | Move the branch pointer to a previous commit, `discarding all changes`   | Commit-level                  | No                 | `git reset --hard HEAD~1`         |