# Mission 6 - Git and GitHub

## 1. Task / objective

Practise the basic Git workflow, inspect this repository, and explain how commits, branches and Pull Requests help people work on a project.

## 2. Work completed

I checked the repository before writing this README. These were the outputs at the start of Mission 6:

```text
$ git status --short --branch
## main...origin/main

$ git log --oneline -5
c56e26a Build number converter and practise data representation
07a18fd Run hello.py and compare compilers and interpreters
8ad071a Document operating system and file management
24298a5 Complete Terminal and file management mission
ca61f46 Complete computer basics and IPOS mission

$ git branch -a
* main
  remotes/origin/main

$ git remote -v
origin  https://github.com/[redacted]/digital-detective-8533.git (fetch)
origin  https://github.com/[redacted]/digital-detective-8533.git (push)
```

`origin` is the name of the GitHub remote for this repository. I staged and committed this Mission 6 README locally on `main` after taking that snapshot.

The branch and Pull Request activity is still pending: `update-about` was not in the branch list, so it has not been created or pushed in this checkpoint. The “My Learning” section has not been added to the root README, and a PR has not been opened. I have kept this change limited to the Mission 6 README as requested.

### Basic Git workflow

| Git operation | What it does in my own words |
|---|---|
| Check status | `git status` shows which files are changed, staged or untracked. |
| Stage a file | `git add mission-06-git-github/README.md` selects this change for the next commit. |
| Commit changes | `git commit` saves the staged snapshot with a message and commit ID. |
| View history | `git log --oneline` shows recent commits in a short list. |

### Branches and Pull Requests

A branch is a named line of work that can move forward separately from `main`. The assignment's `update-about` branch is meant for a short “My Learning” change to the root README. A Pull Request asks for that branch's changes to be reviewed and merged into `main`; it gives people a place to discuss the change before it becomes part of the main line. The PR is not open yet because the branch has not been created or pushed.

### Git command glossary

- `git init` - starts tracking a folder as a new Git repository.
- `git status` - shows what has changed and what is staged.
- `git add <file>` - stages the selected file for a commit.
- `git commit -m "message"` - records the staged changes as a commit.
- `git log --oneline` - shows the commit history in a compact form.
- `git branch -a` - lists local and known remote branches.
- `git switch <branch>` - moves to another branch.
- `git push` - sends local commits or a branch to the remote repository.
- `git pull` - gets remote changes and integrates them into the current branch.

## 3. Commands / tools used

- `git status --short --branch` - checked the working tree and branch tracking state.
- `git log --oneline -5` - inspected the five most recent commits.
- `git branch -a` - checked which local and remote branches were available.
- `git remote -v` - checked the remote name and fetch/push destinations; the owner name is redacted here.
- `git add` and `git commit` - staged and saved only this mission README.

## 4. My understanding

A repository is the project files together with Git's history. Git notices file changes in the working folder. I choose which changes to include with `git add`; those selected changes go into a staging area. A commit records that staged snapshot, so staging and committing are two separate steps.

A commit has a message and an ID, which makes it easier to see what changed later. A branch is a movable name for a line of commits, and a remote is the saved connection to another copy of the repository, such as GitHub's `origin`. Git does not save every keystroke; it records the chosen state when I commit.

## 5. Difficulties faced

I expected to see the `update-about` branch in the branch list, but `git branch -a` showed only `main` and `origin/main`. I was unsure whether the branch was missing locally or on GitHub.

## 6. How I resolved them

I checked both the local and known remote branches with `git branch -a`. Since `update-about` was not listed, I recorded the branch and PR steps as pending instead of saying they were complete. The Mission 6 README itself is staged and committed on `main`.

## 7. Evidence / files

- This README contains the repository inspection output, Git explanations and current branch/PR status.
- No Mac username, device name or serial number is included.

## 8. Commit details

- Commit message: `Complete Git and GitHub collaboration mission`
- Status: committed locally on `main`; not pushed to GitHub.
- Pull Request status: not opened; the `update-about` branch still needs to be created and published.
