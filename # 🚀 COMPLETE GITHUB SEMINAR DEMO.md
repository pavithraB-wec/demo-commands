 # 🚀 COMPLETE GITHUB SEMINAR DEMO

## 👑 Owner: Pavi

## 🤖 Contributor: Ranjana

### Project

Use your existing repository:

```text
cse-github-seminar
```

And your two files:

```text
owner.html
contributor.html
README.md
```

---

# PART 1 — 👑 PAVI: Prepare the Repository

## Step 1 — Check Git

On Pavi's computer:

```bash
git --version
```

Expected:

```text
git version 2.x.x
```

Explain:

> "This verifies that Git is installed."

---

## Step 2 — Configure Git

Only needed once on the computer:

```bash
git config --global user.name "Pavi"
git config --global user.email "your-email@example.com"
```

Check:

```bash
git config --list
```

Your notes specifically cover Git installation, username/email configuration, configuration levels, and checking settings. 

---

# PART 2 — 👑 PAVI: Create Repository

Create the repository on GitHub:

```text
cse-github-seminar
```

Initialize with:

```text
README.md
```

Then clone it.

```bash
git clone https://github.com/pavithraB-wec/cse-github-seminar.git
```

Enter the folder:

```bash
cd cse-github-seminar
```

---

# PART 3 — 👑 PAVI: Understand the 4 Git Areas

Explain this before commands:

```text
Working Directory
       │
       │ git add
       ↓
Staging Area
       │
       │ git commit
       ↓
Local Repository
       │
       │ git push
       ↓
Remote Repository
      GitHub
```

This four-stage architecture is shown in your uploaded notes. 

---

# PART 4 — 👑 PAVI: Check Repository

```bash
git status
```

Then:

```bash
git branch
```

Then:

```bash
git remote -v
```

Expected:

```text
origin  https://github.com/pavithraB-wec/cse-github-seminar.git
```

Explain:

* `git status` → current state
* `git branch` → branches
* `git remote -v` → connected GitHub repository

---

# PART 5 — 👑 PAVI: Add Owner Page

Put your `owner.html` into the repository.

Then:

```bash
git status
```

You should see:

```text
Untracked files:
    owner.html
```

Now:

```bash
git add owner.html
```

Check:

```bash
git status
```

Then:

```bash
git commit -m "Add owner page"
```

Check history:

```bash
git log --oneline
```

Finally:

```bash
git push origin main
```

### Explain the sequence:

```text
owner.html
    ↓
git add
    ↓
Staging
    ↓
git commit
    ↓
Local Repository
    ↓
git push
    ↓
GitHub
```

This demonstrates the core `add → commit → push` lifecycle from your notes. 

---

# PART 6 — 👑 PAVI: Add Ranjana as Contributor

On GitHub:

```text
Repository
   ↓
Settings
   ↓
Collaborators
   ↓
Add people
   ↓
Ranjana's GitHub username
```

Ranjana accepts the invitation.

Now you have:

```text
             cse-github-seminar
                    │
              ┌─────┴─────┐
              ↓           ↓
           Pavi        Ranjana
          Owner       Contributor
```

---

# PART 7 — 🤖 RANJANA: Clone Repository

Now switch to **Ranjana's computer**.

```bash
git clone https://github.com/pavithraB-wec/cse-github-seminar.git
```

Then:

```bash
cd cse-github-seminar
```

Check:

```bash
git status
```

Then:

```bash
git branch
```

Expected:

```text
* main
```

---

# PART 8 — 🤖 RANJANA: Pull Latest Changes

Before working:

```bash
git pull origin main
```

If everything is current:

```text
Already up to date.
```

Explain:

> "`git pull` gets the latest changes from the remote repository and integrates them into the current branch."

Your notes distinguish **fetch, pull and push**, with pull described as fetching and merging remote changes. 

---

# PART 9 — 🤖 RANJANA: Create Branch

Do NOT work directly on `main`.

Create:

```bash
git switch -c feature-contributor
```

Check:

```bash
git branch
```

Expected:

```text
* feature-contributor
  main
```

You can also demonstrate the older command:

```bash
git checkout -b feature-contributor
```

But don't run both. They're alternatives.

Your notes cover creating, switching, renaming and deleting branches. 

---

# PART 10 — 🤖 RANJANA: Create Contributor Page

Ranjana creates:

```text
contributor.html
```

Then:

```bash
git status
```

Output:

```text
Untracked files:
    contributor.html
```

---

# PART 11 — 🤖 RANJANA: `git add`

```bash
git add contributor.html
```

Or:

```bash
git add .
```

Check:

```bash
git status
```

Now it should show:

```text
Changes to be committed:
    new file: contributor.html
```

Explain:

> "`git add` moves changes from the working directory to the staging area."

---

# PART 12 — 🤖 RANJANA: `git commit`

```bash
git commit -m "Add contributor page"
```

Then:

```bash
git log --oneline
```

You should see something similar to:

```text
a82f123 Add contributor page
...
```

Explain:

> "`git commit` saves the staged changes in the local repository."

---

# PART 13 — 🤖 RANJANA: `git push`

```bash
git push -u origin feature-contributor
```

The `-u` sets the upstream tracking relationship.

After this, GitHub will contain:

```text
main
│
└── feature-contributor
```

This is exactly the stage you reached in your current demo. 👍

---

# PART 14 — 🤖 RANJANA: Create Pull Request

Go to GitHub.

You should see:

```text
Compare & pull request
```

Click it.

Set:

```text
base: main
compare: feature-contributor
```

Title:

```text
Add Contributor Page
```

Description:

```text
Added the contributor page for the GitHub collaboration seminar.
```

Click:

**Create Pull Request**

---

# PART 15 — 👑 PAVI: Review Pull Request

Now Pavi opens:

```text
Pull Requests
      ↓
Add Contributor Page
```

Go to:

```text
Files changed
```

Check:

* HTML
* CSS
* Links
* Content
* No unwanted files
* No passwords/API keys

Your source notes explicitly include code review, feedback and reviewing before merging. 

---

# PART 16 — 👑 PAVI: Approve

If everything is correct:

```text
Review changes
       ↓
Approve
       ↓
Submit review
```

Then:

```text
Merge pull request
       ↓
Confirm merge
```

Now:

```text
feature-contributor
        │
        ↓
      MERGE
        │
        ↓
       main
```

---

# PART 17 — 🤖 RANJANA: Get the Merged Changes

After Pavi merges:

```bash
git switch main
```

Then:

```bash
git pull origin main
```

Now Ranjana's local `main` contains:

```text
owner.html
contributor.html
README.md
```

🎉 **Your main collaboration demonstration is complete.**

---

# 🔥 NOW DEMONSTRATE THE OTHER GIT COMMANDS

Don't try to force every command into the main PR flow. Instead, after the main workflow, say:

> "Now that we understand the normal workflow, let's see the commands developers use when their workflow becomes more complex."

---

# 18. 🔎 `git fetch`

On Ranjana's computer:

```bash
git fetch origin
```

Then:

```bash
git status
```

Explain:

```text
git fetch
     ↓
Downloads remote information
     ↓
Does NOT automatically merge
```

Compare:

```text
FETCH
GitHub ─────→ Local tracking information

PULL
GitHub ─────→ Fetch + integrate into current branch
```

Your notes explicitly distinguish `fetch` from `pull`. 

---

# 19. 🧳 `git stash`

This is a very good live demo.

Ranjana modifies `contributor.html` but does **not commit**.

```bash
git status
```

Now suppose Pavi asks:

> "Quickly switch to another branch."

Instead of committing unfinished work:

```bash
git stash
```

Check:

```bash
git status
```

The working tree should become clean.

See saved stashes:

```bash
git stash list
```

Switch branch:

```bash
git switch main
```

Later return:

```bash
git switch feature-contributor
```

Restore the work:

```bash
git stash apply
```

Explain:

> "`git stash` temporarily stores unfinished changes so I can switch branches without committing incomplete work."

Your notes cover `stash`, `stash list`, `stash apply`, `stash drop`, and `stash clear`. 

---

# 20. 🔀 `git merge`

Create a test branch:

```bash
git switch -c feature-merge-demo
```

Make a small change.

```bash
git add .
git commit -m "Demo merge"
```

Return:

```bash
git switch main
```

Merge:

```bash
git merge feature-merge-demo
```

Now:

```text
main
 │
 ├── original commits
 │
 └──── feature changes
```

Explain:

> "`git merge` combines changes from one branch into another."

---

# 21. 🔄 `git rebase`

This should be a **controlled demonstration**, not something you do on your real shared `main`.

Create:

```bash
git switch -c feature-rebase-demo
```

Make a commit.

Then switch to main and make another commit:

```bash
git switch main
```

Make change:

```bash
git add .
git commit -m "Update main"
```

Go back:

```bash
git switch feature-rebase-demo
```

Then:

```bash
git rebase main
```

Explain:

```text
MERGE
→ preserves branch history
→ may create merge commit

REBASE
→ replays feature commits on latest main
→ creates a cleaner linear history
```

Your source specifically compares merge and rebase and advises avoiding rebase on shared branches. 

---

# 22. 🌿 `git branch`

Show all local branches:

```bash
git branch
```

Show remote branches:

```bash
git branch -r
```

Show both:

```bash
git branch -a
```

---

# 23. ✏️ Rename a Branch

Create:

```bash
git switch -c old-feature
```

Rename:

```bash
git branch -m new-feature
```

Check:

```bash
git branch
```

Explain:

> "`-m` renames the current branch."

---

# 24. 🗑️ Delete a Branch

After merging a test branch:

```bash
git branch -d feature-merge-demo
```

If you deliberately need to delete an unmerged local test branch:

```bash
git branch -D test-branch
```

⚠️ Explain that `-D` forces deletion, so it should be used carefully.

Your source notes distinguish safe deletion with `-d` and forced deletion with `-D`. 

---

# 25. 📜 `git log`

Basic history:

```bash
git log
```

Compact:

```bash
git log --oneline
```

Graph:

```bash
git log --oneline --graph --all
```

This is excellent for your seminar because students can **visually see branches and merges**.

---

# 26. 🔍 `git diff`

Make a change but don't commit.

Then:

```bash
git diff
```

This shows:

```text
old line
new line
```

After staging:

```bash
git add .
```

Then:

```bash
git diff --staged
```

Explain:

```text
git diff
       ↓
Working directory vs staging

git diff --staged
       ↓
Staging vs last commit
```

Your uploaded notes explicitly include both forms. 

---

# 27. 🔗 Remote Commands

Show:

```bash
git remote -v
```

Add a remote in a test repository:

```bash
git remote add origin <repository-url>
```

Rename remote:

```bash
git remote rename origin upstream
```

Remove:

```bash
git remote remove upstream
```

Don't run these unnecessarily on your actual seminar repository—use a small practice folder if you want to demonstrate them.

Your notes cover adding, removing, renaming and changing remote URLs. 

---

# 28. 🏷️ Git Tags

Tags are useful for marking versions/releases.

Create:

```bash
git tag v1.0
```

See tags:

```bash
git tag
```

Create annotated tag:

```bash
git tag -a v1.1 -m "Version 1.1"
```

Show tag:

```bash
git show v1.1
```

Push tag:

```bash
git push origin v1.1
```

Or all tags:

```bash
git push --tags
```

Your notes cover lightweight and annotated tags and pushing tags. 

---

# 29. 🍒 `git cherry-pick`

This is an advanced but impressive demo.

Suppose another branch contains one useful commit.

Find its ID:

```bash
git log --oneline
```

Example:

```text
a82f123 Add contributor page
```

On another branch:

```bash
git cherry-pick a82f123
```

Explain:

> "`cherry-pick` takes one specific commit and applies it to the current branch."

Your source notes explicitly include cherry-pick as an advanced topic. 

---

# 30. ↩️ `git restore`

Make an unwanted change.

Then:

```bash
git restore contributor.html
```

This discards the uncommitted working-directory changes to that file.

For an unstaging demonstration:

```bash
git restore --staged contributor.html
```

Explain:

> "`restore` is used to discard or unstage changes."

Your source notes include `restore` for working-directory and staged changes. 

---

# 31. ⏪ `git reset`

This is where you should be careful.

For a **safe seminar demonstration**, use a temporary branch.

Check commits:

```bash
git log --oneline
```

Then demonstrate:

```bash
git reset --soft HEAD~1
```

Explain:

> "`--soft` moves HEAD back but keeps the changes staged."

Then you can restore the state with another commit.

You can explain the other modes:

```text
--soft
Keep changes staged

--mixed
Keep changes but unstage them

--hard
Discard changes
```

⚠️ **Do not demonstrate `git reset --hard` on your real `main` branch during the seminar.**

Your uploaded recovery notes specifically distinguish reset modes and warn about destructive use. 

---

# 32. ↩️ `git revert`

This is safer for shared history.

Find a commit:

```bash
git log --oneline
```

Then:

```bash
git revert <commit-id>
```

Git creates a **new commit that undoes the earlier commit**.

Explain:

```text
reset
→ moves history

revert
→ creates a new undo commit
```

Your source notes recommend `revert` for undoing commits on shared/public branches. 

---

# 33. 🧭 `git reflog`

This is your **recovery demo**.

Run:

```bash
git reflog
```

You'll see HEAD movements such as:

```text
HEAD@{0}
HEAD@{1}
HEAD@{2}
```

Explain:

> "`reflog` records movements of HEAD and can help recover commits that seem lost after operations such as reset or rebase."

Your source notes specifically identify reflog as a recovery tool. 

---

# 34. ⚔️ MERGE CONFLICT DEMO

This would be an excellent ending to your seminar.

Have **Pavi and Ranjana edit the same line** differently.

For example:

### Pavi's version

```html
<h1>GitHub Owner</h1>
```

### Ranjana's version

```html
<h1>GitHub Contributor</h1>
```

Both modify the same line in separate branches.

When you merge, Git may show:

```text
CONFLICT
```

The file may contain:

```text
<<<<<<< HEAD
<h1>GitHub Owner</h1>
=======
<h1>GitHub Contributor</h1>
>>>>>>> feature-contributor
```

Explain:

```text
<<<<<<< HEAD
Your current branch

=======
Other branch

>>>>>>> branch-name
```

Edit the file and keep the desired final version.

Then:

```bash
git add .
```

Commit:

```bash
git commit -m "Resolve merge conflict"
```

This demonstrates a real-world problem rather than only the happy path. Your source notes include the conflict workflow: identify the conflict, edit/resolve, save, stage and commit. 

---

# 🏆 YOUR FINAL SEMINAR FLOW

Don't present 30 commands randomly. Present them in **levels**.

## LEVEL 1 — Basic Git

### 👑 Pavi

```bash
git --version
git config --global user.name "Pavi"
git config --global user.email "..."
```

### Repository

```bash
git init
git status
git remote -v
```

### Basic workflow

```bash
git add .
git commit -m "message"
git log --oneline
git push
```

---

# LEVEL 2 — 🤖 Ranjana Collaboration

```bash
git clone <url>
git pull origin main
git switch -c feature-contributor
```

Then:

```bash
git add .
git commit -m "Add contributor page"
git push -u origin feature-contributor
```

Then:

```text
Pull Request
     ↓
Pavi reviews
     ↓
Approve
     ↓
Merge
```

Then:

```bash
git switch main
git pull origin main
```

---

# LEVEL 3 — Branching

Demonstrate:

```bash
git branch
git branch feature-test
git switch feature-test
git switch main
git merge feature-test
git branch -d feature-test
```

Also show:

```bash
git log --oneline --graph --all
```

---

# LEVEL 4 — Remote Operations

```bash
git remote -v
git fetch origin
git pull origin main
git push origin main
```

Explain the difference:

```text
FETCH = Download information, don't merge

PULL = Fetch + integrate

PUSH = Upload local commits
```

---

# LEVEL 5 — Advanced

Demonstrate:

```bash
git stash
git stash list
git stash apply

git tag v1.0
git show v1.0

git cherry-pick <commit-id>

git rebase main

git restore <file>

git revert <commit-id>

git reflog
```

---

# 🎬 FINAL LIVE STORY

This is the sequence I'd actually use for your seminar:

```text
                 👑 PAVI
              Repository Owner
                     │
                     ↓
              Create GitHub Repo
                     │
                     ↓
                git init
                     │
                     ↓
                git add .
                     │
                     ↓
               git commit
                     │
                     ↓
               git push
                     │
                     ↓
              Add Ranjana
                     │
                     ↓
              🤖 RANJANA
                     │
                     ↓
                 git clone
                     │
                     ↓
              git pull origin main
                     │
                     ↓
          git switch -c feature-contributor
                     │
                     ↓
                Make changes
                     │
                     ↓
                 git status
                     │
                     ↓
                  git add
                     │
                     ↓
                 git commit
                     │
                     ↓
                  git push
                     │
                     ↓
             Pull Request
                     │
                     ↓
                👑 PAVI
                     │
                     ↓
                Code Review
                  /       \
                 /         \
            ❌ Changes    ✅ Approve
                │             │
                ↓             ↓
            Ranjana        MERGE
             fixes           │
                │             ↓
                └────────→   main
                              │
                              ↓
                     🤖 Ranjana
                              │
                              ↓
                    git pull origin main
                              │
                              ↓
                       Latest Project
```

Then finish with:

```text
        🚨 PROBLEM SCENARIOS

        Modified file
             ↓
          git stash
             ↓
        switch branch

        Remote changes
             ↓
          git fetch
             ↓
          git pull

        Branch conflict
             ↓
          git merge
             ↓
       Resolve conflict

        Need clean history
             ↓
          git rebase

        Need one commit
             ↓
       git cherry-pick

        Need undo
          ↙       ↘
      restore    revert
                   ↓
              Shared branch

        Lost commit
             ↓
          git reflog
```

## 🧠 The commands your audience should leave remembering

| Command           | One-line meaning                            |
| ----------------- | ------------------------------------------- |
| `git init`        | Create a Git repository                     |
| `git clone`       | Copy remote repository locally              |
| `git status`      | Check current changes                       |
| `git add`         | Stage changes                               |
| `git commit`      | Save changes locally                        |
| `git push`        | Send commits to remote                      |
| `git pull`        | Fetch + integrate remote changes            |
| `git fetch`       | Download remote information without merging |
| `git branch`      | Manage branches                             |
| `git switch`      | Switch/create branches                      |
| `git checkout`    | Older multi-purpose branch/file command     |
| `git merge`       | Combine branches                            |
| `git rebase`      | Replay commits on a new base                |
| `git stash`       | Temporarily store unfinished changes        |
| `git tag`         | Mark a version/release                      |
| `git cherry-pick` | Apply one specific commit                   |
| `git restore`     | Restore/unstage changes                     |
| `git reset`       | Move HEAD / undo local history              |
| `git revert`      | Undo with a new commit                      |
| `git reflog`      | Recover/find previous HEAD positions        |

