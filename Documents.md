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
# Git Workflow Example

```bash
# Initialize Git repository
mkdir myproject
cd myproject
git init

---
# Add a file a.txt
echo "First file content" > a.txt
git add a.txt
---
# Make a commit
git commit -m "Added a.txt"
# Create a branch called leaf
git checkout -b leaf
# Add a file b.txt
echo "Second file content" > b.txt
git add b.txt
# Create a second commit
git commit -m "Added b.txt in leaf branch"
# Merge leaf into master
git checkout master
git merge leaf

---

## 6. Best Practices for Collaboration

- Use branches for features/bug fixes.
- Write clear commit messages (imperative style: “Add login form”).
- Pull often to stay updated with team changes.
- Keep the `main` branch stable (merge only tested code).
- Use `.gitignore` to avoid committing unnecessary files.
- Review code via pull requests before merging.

---

