
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

## 3. Git Workflow Example
### Initialize Git repository

```bash
mkdir myproject
cd myproject
git init
```
### Add a file a.txt

```bash
echo "First file content" > a.txt
git add a.txt
```
### Make a commit

```bash
git commit -m "Added a.txt"
```
### Create a branch called leaf

```bash
git checkout -b leaf
```
### Add a file b.txt

```bash
echo "Second file content" > b.txt
git add b.txt
```
### Create a second commit

```bash
git commit -m "Added b.txt in leaf branch"
```
### Merge leaf into master

```bash
git checkout master
git merge leaf
```

---

## 4. Best Practices for Collaboration

- Use branches for features/bug fixes.
- Write clear commit messages (imperative style: “Add login form”).
- Pull often to stay updated with team changes.
- Keep the `main` branch stable (merge only tested code).
- Use `.gitignore` to avoid committing unnecessary files.
- Review code via pull requests before merging.
```

Would you like me to also add a **section on handling merge conflicts** (like in your earlier file) so this becomes a complete beginner-friendly guide?
