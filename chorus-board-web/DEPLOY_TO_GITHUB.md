# Deploying Chorus Board to GitHub Pages

A step-by-step guide to get your web app live at `yourusername.github.io/chorus-board`

---

## Prerequisites

- A GitHub account (free) at https://github.com
- The `chorus-board-web` folder containing `index.html`

---

## Step 1: Create a GitHub Repository

1. Go to https://github.com/new
2. Fill in:
   - **Repository name:** `chorus-board`
   - **Description:** Chorus Board Generator - paste lyrics, download PowerPoint
   - **Visibility:** Public (required for free GitHub Pages)
   - **Do NOT** check "Add a README" — we'll push our own files
3. Click **"Create repository"**

You'll see a page with setup instructions. Keep this tab open.

---

## Step 2: Upload Your Files

**Option A — Upload via GitHub website (easiest, no Git needed):**

1. On your new repo page, click **"uploading an existing file"** link
2. Drag and drop the `index.html` file from your `chorus-board-web` folder
3. In "Commit changes", type: `Initial commit - chorus board generator`
4. Click **"Commit changes"**

**Option B — Using Git command line (for learning):**

```bash
# Open Terminal, navigate to the folder
cd ~/Desktop/Claude\ Work/MDH/chorus-board-web

# Initialize git
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit - chorus board generator"

# Connect to your GitHub repo (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/chorus-board.git

# Push
git branch -M main
git push -u origin main
```

If asked to log in, enter your GitHub username and a Personal Access Token
(GitHub > Settings > Developer settings > Personal access tokens > Generate new token).

---

## Step 3: Enable GitHub Pages

1. In your repo, click **"Settings"** (gear icon, top menu)
2. In the left sidebar, click **"Pages"**
3. Under **"Source"**, select:
   - **Branch:** `main`
   - **Folder:** `/ (root)`
4. Click **"Save"**

GitHub will show: *"Your site is live at https://YOUR_USERNAME.github.io/chorus-board/"*

It takes 1–2 minutes for the first deploy. Refresh the page if you don't see the URL yet.

---

## Step 4: Visit Your Live Site

Open: `https://YOUR_USERNAME.github.io/chorus-board/`

That's it — your Chorus Board Generator is live. Share this URL with anyone who needs it.

---

## Updating the Site Later

When you want to make changes:

**Via GitHub website:**
1. Go to your repo on GitHub
2. Click on `index.html`
3. Click the pencil icon (Edit)
4. Make your changes
5. Click **"Commit changes"**
6. Site updates automatically in ~1 minute

**Via Git command line:**
```bash
cd ~/Desktop/Claude\ Work/MDH/chorus-board-web
git add .
git commit -m "Description of what you changed"
git push
```

---

## Quick Reference

| What | Where |
|------|-------|
| Your repo | `github.com/YOUR_USERNAME/chorus-board` |
| Your live site | `YOUR_USERNAME.github.io/chorus-board` |
| Edit files | Repo > click file > pencil icon |
| Settings | Repo > Settings > Pages |
| Cost | Free, forever |
| Limits | 100GB bandwidth/month (plenty) |

---

## Troubleshooting

**Site shows 404:**
- Check Settings > Pages — is the source set to `main` branch, `/ (root)`?
- Wait 2 minutes and refresh. First deploy can be slow.

**Changes not showing:**
- Hard refresh: Cmd+Shift+R (Mac) or Ctrl+Shift+R (Windows)
- Check the "Actions" tab in your repo — you'll see deployment status

**Need a custom domain (optional):**
- Settings > Pages > Custom domain
- Enter your domain and follow the DNS instructions
