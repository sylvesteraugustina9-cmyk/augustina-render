# Augustina — Web Developer Portfolio

A simple HTML/CSS/JS portfolio site connected to Supabase for feedback, hosted on Render with a manual GitHub Actions CI/CD pipeline.

---

## 📁 Project Structure

```
my-portfolio/
├── index.html                  ← Main portfolio page
├── profile.jpeg                ← Your profile photo (rename to this)
├── README.md                   ← This file
└── .github/
    └── workflows/
        └── deploy.yml          ← GitHub Actions manual deploy pipeline
```

---

## 🚀 Deployment Setup (One-Time)

### 1. Push to GitHub
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/my-portfolio.git
git push -u origin main
```

### 2. Create Static Site on Render
- Go to https://render.com → New → Static Site
- Connect your GitHub repo
- Build Command: *(leave empty)*
- Publish Directory: `.`
- Click **Create Static Site**

### 3. Get Render Credentials
- **API Key**: Render Dashboard → Avatar → Account Settings → API Keys → Create
- **Service ID**: From the URL when viewing your site: `srv-XXXXXXXXXX`

### 4. Add GitHub Secrets
Go to your repo → Settings → Secrets and variables → Actions:

| Secret Name         | Value                  |
|---------------------|------------------------|
| `RENDER_API_KEY`    | Your Render API key    |
| `RENDER_SERVICE_ID` | Your `srv-XXXXXXXXXX`  |

---

## ▶️ How to Deploy

1. Go to your GitHub repo → **Actions** tab
2. Click **"Deploy to Render"** in the left sidebar
3. Click **"Run workflow"** → add an optional reason → **Run workflow**
4. Watch the logs — it will poll until your site is live ✅

---

## 🖼️ Profile Image

Rename your profile photo to `profile.jpeg` and place it in the root folder alongside `index.html`.

---

© 2026 Augustina
