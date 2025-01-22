# Terminology
- git: an open source, distributed version-control system
- GitHub: a platform for hosting and collaborating on Git repositories
- commit: a Git object, a snapshot of your entire repository compressed into a SHA
- branch: a lightweight movable pointer to a commit
- clone: a local version of a repository, including all commits and branches
- remote: a common repository on GitHub that all team members use to exchange their changes
- fork: a copy of a repository on GitHub owned by a different user
- pull request: a place to compare and discuss the differences introduced on a branch with reviews, comments, integrated tests, and more
- HEAD: representing your current working directory, the HEAD pointer can be moved to different branches, tags, or commits when using git switch

# Basic Workflow

### Add File to Staging
```bash
git add <file>
git add .
```

### Commit Changes
```bash
git commit -m "Your message"
```

### Push Changes to Remote
```bash
git push origin <branch-name>
```

### Pull Changes from Remote
```bash
git pull origin <branch-name>
```

---

# Branching

### Show all branches
```bash
git branch -a
```

### Creates a new branch
```bash
git branch <branch-name>
```

### Switches to the specified branch and updates the working directory
```bash
git switch -c <branch-name>
```

### Undo Changes in a File
```bash
git checkout -- <file>
```

### Reset Staged Changes
```bash
git reset <file>
```

### Amend the Last Commit
```bash
git commit --amend -m "New commit message"
```

---

# Viewing History

### View Commit History
```bash
git log
```

### View a Specific Commit
```bash
git show <commit-hash>
```

---

# Collaboration

### Working with Pull Requests

#### Create a Pull Request:
1. Push your branch to the remote repository:
   ```bash
   git push origin <branch-name>
   ```
2. Open the repository on GitHub (or another hosting service).
3. Navigate to the "Pull Requests" tab.
4. Click "New Pull Request" and select the branches to compare.

#### Review a Pull Request:
1. Navigate to the "Pull Requests" tab on the repository.
2. Select a pull request to review.
3. Provide feedback, approve, or request changes.

#### Merge a Pull Request:
1. Once approved, merge the pull request using the "Merge" button.
2. Optionally, delete the branch after merging.

### Add a Remote Repository
```bash
git remote add origin <repository-url>
```

### View Remotes
```bash
git remote -v
```

### Push for the First Time
```bash
git push -u origin <branch-name>
```

---

# Stash Changes

### Temporarily Save Changes Without Committing
```bash
git stash
```

### Apply Stashed Changes
```bash
git stash apply
```

### Delete a Branch
```bash
git branch -d <branch-name>    # Only if fully merged
git branch -D <branch-name>    # Force delete
```

### Rebase a Branch
```bash
git rebase <branch-name>
