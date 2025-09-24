# My Favorites App

A simple, robust web app to track your favorite project URLs, files, and GitHub repositories. Works entirely client-side—no login, no backend, just your browser!

---

## Features
- **Add, edit, and rate favorites** (1-5 stars)
- **GitHub integration:**
  - Fetch repo info by `username/repo`
  - Browse all public repos by username
  - Choose between the repo URL and the GitHub Pages URL
  - Remembers your last GitHub username for quick searches
  - Smart rating suggestions based on stars
- **Robust data persistence:**
  - Export/import favorites as JSON
  - Create a backup URL you can bookmark or share
  - Detects possible data loss (e.g., iOS Safari clearing localStorage)

---

## How-To: User Guide

### 1. Add a Favorite
- Click **➕ Add New Favorite**
- Enter a title, URL, and rating
- Click **Add Favorite**

### 2. Add a GitHub Repo
- Click the 🐱 button next to the URL field to enter **GitHub Mode**
- Enter `username/repo` (e.g., `junkerfamily/MyFavorites`) or just your username to browse all your repos
- Click **Fetch Info** or **Browse User Repos**
- Choose between the **GitHub Pages URL** (live site) or **Repository URL** (source code)
- The app will auto-fill the title, URL, and suggest a rating

### 3. Export/Import/Backup
- Use **Export** to save your favorites as a file
- Use **Import** to restore from a file
- Use **Backup Link** to create a URL you can bookmark or share (contains your data)

### 4. Data Loss Warning
- If your favorites disappear (e.g., on iOS), the app will warn you and suggest restoring from a backup or export

---

## Advanced Tips

### Private Repos & GitHub Pages
- **GitHub API only shows public repos** (unless you authenticate, which this app does not do)
- **Private repos will NOT appear in the repo browser or search**
- **However, if you know your private repo has a public GitHub Pages site, you can manually construct the URL:**
  - The pattern is: `https://username.github.io/reponame/`
  - Example: If your public repo is `junkerfamily/MyFavorites` (GitHub Pages: `https://junkerfamily.github.io/MyFavorites/`), and your private repo is `junkerfamily/EZ_Message`, you can try `https://junkerfamily.github.io/EZ_Message/` (if the site is published)
  - **Just add this URL manually as a favorite!**
- **Pro tip:** You can base your GitHub Pages URL off a public repo, then change the repo name in the URL to match your private repo (if you know the site is published)

---

## FAQ

**Q: Why can't I find my private repo in the search?**
A: GitHub's public API only returns public repositories. Private repos are hidden for privacy. You can still add their URLs manually if you know them.

**Q: My favorites disappeared!**
A: Some browsers (especially iOS Safari) may clear localStorage. Use Export or Backup Link to prevent data loss.

**Q: Can I use this app offline?**
A: Yes! Once loaded, it works offline (except for GitHub API features).

---

## License
MIT. No warranty. Use at your own risk.
