# Git Rebase Workflow Guide

## 1. Initialize a Repository

```bash
mkdir rebase-demo
cd rebase-demo
git init
```
---
## 1. Initialize a Repository

```bash
mkdir rebase-demo
cd rebase-demo
git init
```

---

## 2. Create the First Commit (M1: Initial project setup)

```bash
echo "Project setup files" > setup.txt
git add setup.txt
git commit -m "M1: Initial project setup"
```

---

## 3. Add Another Commit on Master

```bash
echo "Main branch content" > main.txt
git add main.txt
git commit -m "M2: Add main branch file"
```

---

## 4. Create a Feature Branch

```bash
git checkout -b feature
```

---

## 5. Add Commits on Feature Branch

```bash
echo "Feature work step 1" > feature1.txt
git add feature1.txt
git commit -m "F1: Add feature1 file"

echo "Feature work step 2" > feature2.txt
git add feature2.txt
git commit -m "F2: Add feature2 file"
```

---

## 6. Add a Hotfix on Master

```bash
git checkout master
echo "Hotfix applied" > hotfix.txt
git add hotfix.txt
git commit -m "M3: Apply hotfix"
```

---

## 7. Rebase Feature onto Master

```bash
git checkout feature
git rebase master
```

---
9. Verify History
```bash

git log --oneline 


```

