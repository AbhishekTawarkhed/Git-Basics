# Introduction to Git

## 1. What is Git?
- Git is a distributed version control system (VCS).
- It helps track changes in source code, collaborate with others, and maintain history.
- Key idea: Every developer has a full copy of the repository (not just a snapshot).

---

## 2. Difference between Git, GitHub, and GitLab

- **Git**: A version control system that runs locally on your machine.
- **GitHub**: A cloud-based hosting service for Git repositories. Adds collaboration features like pull requests, issues, and CI/CD.
- **GitLab**: Similar to GitHub but also offers built-in DevOps tools like CI/CD pipelines, project management, and self-hosting options.

---

## 3. Basic Git Commands

### `git init`
Initializes a new Git repository in a folder.

```bash
mkdir myproject
cd myproject
git init
```

---

### `git clone`
Copies an existing repository (from GitHub/GitLab) to your local machine.

```bash
git clone https://github.com/user/repo.git
```

---

### `git add`
Stages changes (prepares them for commit).

```bash
git add file1.txt
git add .
```

---

### `git commit`
Saves staged changes with a message.

```bash
git commit -m "Added new feature"
```

---

### `git push`
Uploads local commits to a remote repository.

```bash
git push origin main
```

---

### `git pull`
Fetches and merges changes from remote.

```bash
git pull origin main
```

---

## 4. Branching and Merging

### Creating a branch
```bash
git branch feature-login
git checkout feature-login
```

Or in one step:
```bash
git checkout -b feature-login
```

---

### Merging a branch
```bash
git checkout main
git merge feature-login
```

---

## 5. Handling Merge Conflicts

When two branches modify the same part of a file differently, Git shows conflict markers:

```text
<<<<<<< HEAD
Your changes
=======
Other branch changes
>>>>>>> feature-login
```

**Steps to resolve:**
1. Edit the file manually to keep the correct changes.
2. Stage the resolved file:
   ```bash
   git add conflicted_file.txt
   ```
3. Commit the resolution:
   ```bash
   git commit
   ```

---

## 6. Best Practices for Collaboration

- Use branches for features/bug fixes.
- Write clear commit messages (imperative style: “Add login form”).
- Pull often to stay updated with team changes.
- Keep the `main` branch stable (merge only tested code).
- Use `.gitignore` to avoid committing unnecessary files.
- Review code via pull requests before merging.

---

