# Tanzim Hossain — Academic Portfolio

> **Live demo:** after deploy, your site will be at `https://tanzim007.github.io/portfolio/`

---

## 📁 What's in this folder

```
tanzim-portfolio/
├── index.html                        ← Entire website (one self-contained file)
├── tanzim_cv.pdf                     ← ⚠️  Replace with YOUR real CV PDF
├── .nojekyll                         ← Tells GitHub Pages to skip Jekyll processing
├── .github/
│   └── workflows/
│       └── deploy.yml                ← Auto-deploys to GitHub Pages on every push
├── assets/
│   └── tanzim.jpg                    ← Profile photo (already embedded in index.html)
└── README.md                         ← This file
```

---

## 🚀 Deploy to GitHub Pages in 3 steps

### Step 1 — Create a GitHub repository
Go to [github.com/new](https://github.com/new) and create a **public** repo.  
Suggested name: `portfolio` (your site will be at `https://tanzim007.github.io/portfolio/`)  
Or name it `tanzim007.github.io` (site will be at `https://tanzim007.github.io/`)

### Step 2 — Upload these files
**Option A — Drag & drop (easiest):**
1. Open your new repo on GitHub
2. Click **"uploading an existing file"** or drag all files from this folder into the browser
3. Click **Commit changes**

**Option B — via Git CLI:**
```bash
cd tanzim-portfolio
git init
git add .
git commit -m "Initial portfolio"
git remote add origin https://github.com/tanzim007/portfolio.git
git branch -M main
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. Go to your repo → **Settings → Pages**
2. Under **Source**, select **GitHub Actions**
3. The workflow (`.github/workflows/deploy.yml`) runs automatically
4. Your site is live in ~1 minute ✅

---

## ✏️ How to update content

All content lives inside **`index.html`** — open it in any text editor (VS Code recommended).

| What to change | Find this in `index.html` |
|---|---|
| Name / bio / title | `#hero` section |
| Research interests | `#research` — add/remove `<div class="interest-card">` blocks |
| Publications | `#publications` — copy/edit `<article class="pub-item">` blocks |
| Projects | `#projects` — edit `<article class="project-card">` blocks |
| CV file | Replace `tanzim_cv.pdf` with your real CV (keep the same filename) |
| Accent color | CSS variable `--accent: #2B5F75;` at the top of `<style>` |

### Adding a publication (example):
```html
<article class="pub-item fade-in">
  <span class="pub-badge conference">Conference · IEEE 2025</span>
  <h3 class="pub-title">Your Paper Title Here</h3>
  <p class="pub-authors"><strong>Hossain T</strong>, Co-Author A, Co-Author B.</p>
  <p class="pub-venue">Conference Name, Year — doi: 10.xxxx/xxxxx</p>
  <div class="pub-links">
    <a href="https://doi.org/..." target="_blank" class="pub-link">DOI →</a>
  </div>
</article>
```

---

## 📧 Enable the contact form (optional)

The form currently falls back to opening your email client.  
To enable server-side submissions (free):
1. Sign up at [formspree.io](https://formspree.io)
2. Create a form → copy the ID (looks like `xpwzqabc`)
3. In `index.html`, find this line and replace `YOUR_FORMSPREE_ID`:
   ```html
   <form ... action="https://formspree.io/f/YOUR_FORMSPREE_ID" ...>
   ```

---

## ▲ Alternative: Deploy to Vercel (even easier)

1. Push to GitHub (Step 2 above)
2. Go to [vercel.com](https://vercel.com) → **Add New → Import Git Repository**
3. Select your repo → click **Deploy**
4. Done — Vercel auto-detects static HTML, no config needed
5. Optionally connect a custom domain in Vercel dashboard

