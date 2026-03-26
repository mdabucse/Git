# Using Git Hooks for Automated Checks

## Overview
This task demonstrates how to use Git hooks to enforce automated checks (like linting or testing) before commits are finalized.

## Steps Performed

1. **Created a `pre-commit` Hook**
   - Added a script in `.git/hooks/pre-commit` to run an HTML linter (`tidy`).

2. **Configured the Hook**
   - The hook checks for HTML linting errors in `index.html`. If errors are found, the commit is aborted.

3. **Tested the Hook**
   - Introduced an error in `index.html` and verified that the commit was blocked.
   - Fixed the error and confirmed that the commit succeeded.

## Repository Structure
```
Task-7/
    index.html
    .git/hooks/pre-commit
```

## Key Commands Used
- `sudo apt-get install tidy`: Installs the `tidy` HTML linter.
- `chmod +x pre-commit`: Makes the hook script executable.
- `git commit -m "message"`: Attempts to commit changes, triggering the hook.