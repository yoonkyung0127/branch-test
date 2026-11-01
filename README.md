# Lecture 9: Remote Branch and Collaboration

This small repository demonstrates the Lecture 9 workflow: create a branch, make independent changes, fetch remote work, resolve a merge conflict, and push the result.

## Example files

- `collaboration.txt` records the final text after a feature change and a main-branch hotfix were merged.
- `workflow.md` lists the commands used for the remote workflow.

## Branch history in this repository

1. `main` starts with a shared version of `collaboration.txt`.
2. `feature/lecture9-update` changes the same sentence to describe the feature.
3. `main` changes that sentence for an urgent correction.
4. Merging the feature branch creates a conflict. The final file keeps both pieces of information, and the merge commit records the resolution.

The commit graph can be inspected with `git log --oneline --graph --all`.
