
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

### Git Configuration

```bash

git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```
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
### Checking Repository Status

```bash

git status
```
### Undoing Changes
```bash
git rm --cached a.txt
```
### Make a commit

```bash
git commit -m "Added a.txt"
```
### Viewing History

```bash

git log
```
### Create a branch called leaf

```bash
git checkout -b leaf
```
or 
```bash
git switch -c leaf
```
### Modify the file a.txt

```bash
echo "Second file content" > a.txt
git add a.txt
```
### Create a second commit

```bash
git commit -m "Modified a.txt in leaf branch"
```
### Switch back to master 
```bash
git checkout master
```
### Modify a.txt differently in master branch and commit 
```bash
echo "Master branch change" > a.txt
git add a.txt
git commit -m "Modified a.txt in master branch"
```
### Merge leaf into master

```bash
git merge leaf
```
### Handling Merge Conflicts

```text
<<<<<<< HEAD
Your changes
=======
Other branch changes
>>>>>>> leaf
```
Edit the file to resolve conflict

```bash
git add a.txt
git commit -m "resolved conflict in a.txt"
```
### Working with Remotes

```bash

git remote add origin https://github.com/user/repo.git
git push -u origin master
```
---

## 4. Best Practices for Collaboration

- Use branches for features/bug fixes.
- Write clear commit messages (“Add login form”).
- Pull often to stay updated with team changes.
- Keep the `main` branch stable (merge only tested code).
- Use `.gitignore` to avoid committing unnecessary files.
- Review code via pull requests before merging.

