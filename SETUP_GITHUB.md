# Create the repo on GitHub and push

The repository **gokikamukow/musictimer** does not exist yet. Create it once, then push this project.

## 1. Create the repository on GitHub

1. Open **https://github.com/new**
2. Set **Repository name** to: `musictimer`
3. Set **Owner** to: `gokikamukow` (or your username if you use a different account)
4. Choose **Public**
5. **Do not** add a README, .gitignore, or license (this project already has them)
6. Click **Create repository**

## 2. Push this project to the new repo

In a terminal, from this project folder, run:

```bash
cd /Users/pholm/sandbox/musictimer

# If this folder is not yet a git repo:
git init
git add -A
git commit -m "Initial commit: Music Timer PWA with GitHub Actions deploy"
git branch -M main

# Add the repo you just created (replace with your actual repo URL if different)
git remote add origin https://github.com/gokikamukow/musictimer.git

# Push
git push -u origin main
```

If the folder is already a git repo with a commit, skip `git init` and the first `git commit`, and run only:

```bash
git remote add origin https://github.com/gokikamukow/musictimer.git
git push -u origin main
```

## 3. Enable GitHub Pages (one-time)

1. Open **https://github.com/gokikamukow/musictimer/settings/pages**
2. Under **Build and deployment**, set **Source** to **GitHub Actions**
3. Save

After the first push, the **Actions** tab will run the deploy workflow. When it finishes, the app will be at **https://gokikamukow.github.io/musictimer/**.
