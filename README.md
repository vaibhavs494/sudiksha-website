# Sudiksha's Website — Setup Guide

## Your folder structure
```
sudiksha-site/
├── index.html              ← the website
├── admin/
│   ├── index.html          ← CMS editor UI
│   └── config.yml          ← defines editable fields
├── content/
│   ├── about.json          ← About Me text, photo, skills
│   ├── gallery.json        ← Art gallery images
│   ├── inspirations.json   ← Inspiration quotes
│   ├── cv.json             ← CV file + stats
│   ├── blog-index.json     ← List of blog posts (update when adding posts)
│   └── blog/
│       └── memory-cafe.json  ← Sample blog post
└── uploads/                ← Images go here (managed by CMS)
```

---

## One-time Setup (takes ~15 minutes)

### Step 1 — Create a GitHub account & repo
1. Go to github.com and create a free account
2. Click "New repository" → name it `sudiksha-website`
3. Set it to **Public**, click Create

### Step 2 — Upload these files to GitHub
1. In your new repo, click "uploading an existing file"
2. Drag in the entire `sudiksha-site` folder contents
3. Click "Commit changes"

### Step 3 — Connect Netlify to GitHub
1. Log into your Netlify account
2. Go to Site Settings → Build & Deploy → Link to Git
3. Choose GitHub → select your `sudiksha-website` repo
4. Build command: leave blank
5. Publish directory: leave blank (or `/`)
6. Click Deploy

### Step 4 — Enable Netlify Identity
1. In Netlify: go to **Identity** tab → click **Enable Identity**
2. Under Registration: set to **Invite only**
3. Under Services → Git Gateway: click **Enable Git Gateway**
4. Go to Identity → click **Invite users** → enter Sudiksha's email
5. She'll get an email to set a password

### Step 5 — Done! 🎉
Sudiksha can now go to `yoursite.netlify.app/admin` to edit everything.

---

## How Sudiksha edits content

1. Go to `yoursite.netlify.app/admin`
2. Log in with her email/password
3. She'll see sections: **About Me**, **Art Gallery**, **Inspirations**, **Blog Posts**, **CV & Stats**
4. Click any section → edit → click **Publish**
5. Changes go live in ~30 seconds automatically

### Adding a new blog post
1. In the CMS, click **Blog Posts** → **New Blog Post**
2. Fill in the title, tag, excerpt, body text
3. Click Publish
4. Then go to **content/blog-index.json** (edit in GitHub) and add the new post's data

> **Note:** The blog-index.json file currently needs to be updated manually in GitHub when adding new posts. This is a known limitation of the free setup — an upgrade path exists if needed.

---

## Adding her artwork photos

Option A (via CMS):
- Go to the CMS → Art Gallery → click each item → upload image

Option B (direct):
- Put image files in the `uploads/` folder in GitHub
- Reference them as `/uploads/your-image.jpg`

---

## Replacing the CV file
1. In the CMS → CV & Stats
2. Upload her PDF using the file picker
3. Hit Publish — the download button updates automatically
