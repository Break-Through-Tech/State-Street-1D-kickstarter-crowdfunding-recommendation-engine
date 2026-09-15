# GitHub Practices

Quick reference for working on this repo as a team.

## Setup (once)

```bash
git clone https://github.com/Break-Through-Tech/State-Street-1D-kickstarter-crowdfunding-recommendation-engine.git
cd <repo-folder>
```

## Making your own branch

Always work on your own branch, not `main`.

```bash
git checkout main
git pull                        # get the latest changes
git checkout -b "your-name-feature"   # e.g. git checkout -b Michelle
```

## Committing your work

```bash
git status                      # see what changed

#important must do all these steps in this order!!!
git add -A                  # or `git add "filename"` to stage one file
git commit -m "short description of what you did"
git push origin your-name-feature #if working on main it would be git push origin main
```

Commit often, in small chunks, with clear messages (e.g. `"clean missing values in goal column"` not `"update"`).

## Opening a Pull Request (PR)

1. Push your branch (see above).
2. Go to the repo on GitHub — you'll see a prompt to open a PR from your branch into `main`.
3. Add a short description of what you changed.
4. Ask a teammate to review before merging.

## Merging

Once your PR is approved:

```bash
# on GitHub: click "Merge pull request"
```

Then update your local `main` and delete the merged branch:

```bash
git checkout main
git pull
git branch -d your-name-feature
```
OR (michelle's not so great way where theres no PR)
- PR just good for documentation tbh and keeping teammates in the loop

```bash
git checkout main #or git switch main 
git pull origin main
git merge feature-branch-name
git push origin main
```

## Switching Branches 

```bash
#if branch already exists
git switch branch-name
```
## Keeping your branch up to date

If `main` changes while you're still working:

```bash
git checkout main
git pull
git checkout your-name-feature
git merge main
```

## Golden rules

- Never commit directly to `main` — always use a branch + PR.
- Pull before you start working.
- Commit small, commit often.
- Write clear commit messages and PR descriptions.
