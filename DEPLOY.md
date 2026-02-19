# Deploy to GitHub (feature → develop → main)

Run these in a terminal from the repo folder. Replace the repo path if yours is different.

## 1. Go to the repo folder

```bash
cd /Users/growingpenguin/Documents/Neurosymbolic_AI/Final_Project/cross-model-neighborhood-consistency
```

## 2. Init and first commit (feature)

```bash
git init -b main
git remote add origin https://github.com/growingpenguin/cross-model-neighborhood-consistency.git
git checkout -b feature
git add .
git commit -m "Add fin8 notebook, result10, pitch, papers"
```

## 3. Push feature, then develop

```bash
git push -u origin feature
git checkout -b develop
git merge feature
git push -u origin develop
```

## 4. Merge to main and push

```bash
git checkout main
git merge develop
git push -u origin main
```

If the GitHub repo already has a commit (e.g. "Add a README"), either:

- Pull first: `git pull origin main --allow-unrelated-histories` on main, then merge, then push; or  
- Overwrite: `git push -u origin main --force` (only if you are fine replacing the remote main).

After the first deploy you can delete this file or keep it for reference.
