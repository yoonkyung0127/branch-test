# Remote branch workflow

Replace `<repository-url>` with the HTTPS URL of the GitHub repository.

## Publish a local repository

```sh
git remote add origin <repository-url>
git push -u origin main
git push -u origin feature/lecture9-update
```

## Clone and make independent changes

```sh
git clone <repository-url> collaborator-copy
cd collaborator-copy
git switch -c feature/lecture9-update
# edit and commit the feature change
git push -u origin feature/lecture9-update
```

## Fetch and merge remote work

In the original working copy:

```sh
git fetch origin
git switch main
git merge origin/feature/lecture9-update
```

If both branches changed the same lines, edit the conflict markers in the affected file, keep the intended combined result, then complete the merge:

```sh
git add collaboration.txt
git commit
git push origin main
```

## Pull shortcut

`git pull` fetches and then integrates the upstream branch. The two-step `git fetch` and `git merge` sequence makes those actions visible separately.
