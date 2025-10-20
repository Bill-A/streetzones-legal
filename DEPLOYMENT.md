# Street•Zones Legal Documentation - Deployment Guide

## 🚀 Quick Start

### Step 1: Create GitHub Repository

Go to: https://github.com/new

**Settings:**
- Repository name: `streetzones-legal`
- Visibility: **PUBLIC** (required for free GitHub Pages)
- ❌ Do NOT check "Add a README file"
- Click "Create repository"

### Step 2: Push to GitHub

Replace `yourusername` with your actual GitHub username:

```bash
cd /Volumes/NVME_Macintosh/SoftwareProjects/streetzones-legal

git remote add origin https://github.com/yourusername/streetzones-legal.git
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to: `https://github.com/yourusername/streetzones-legal/settings/pages`
2. **Source**: Deploy from a branch
3. **Branch**: `main`
4. **Folder**: `/ (root)`
5. Click **Save**

### Step 4: Wait for Deployment

- Deployment takes ~1 minute
- Check deployment status: `https://github.com/yourusername/streetzones-legal/deployments`
- Site will be available at: `https://yourusername.github.io/streetzones-legal/`

---

## 📄 URLs for App Store Submission

After deployment, use these URLs (replace `yourusername`):

**Privacy Policy:**
```
https://yourusername.github.io/streetzones-legal/privacy-policy.html
```

**Terms of Service:**
```
https://yourusername.github.io/streetzones-legal/terms-of-service.html
```

**Accessibility Statement:**
```
https://yourusername.github.io/streetzones-legal/accessibility.html
```

---

## 🔄 Updating Legal Documents

When you need to update legal documents in the future:

```bash
# 1. Update source files in main repo
cd /Volumes/NVME_Macintosh/SoftwareProjects/rn_workspace/street-zone/legal-site
# (Make your edits)

# 2. Re-run setup script to copy updates
bash /Volumes/NVME_Macintosh/SoftwareProjects/rn_workspace/street-zone/scripts/setup-legal-repo.sh

# 3. Push updates to GitHub
cd /Volumes/NVME_Macintosh/SoftwareProjects/streetzones-legal
git add .
git commit -m "Update legal documentation"
git push

# GitHub Pages auto-deploys in ~1 minute
```

---

## ✅ Testing Checklist

After deployment, verify:

- [ ] Landing page loads: `https://yourusername.github.io/streetzones-legal/`
- [ ] Privacy Policy loads and renders correctly
- [ ] Terms of Service loads and renders correctly
- [ ] Accessibility Statement loads and renders correctly
- [ ] Back links work on all 3 legal pages
- [ ] Mobile responsive design works (test on phone)
- [ ] HTTPS is enabled (🔒 in browser)
- [ ] No 404 errors or broken links

---

## 🔒 Security Notes

✅ **Main app repository stays PRIVATE**
- No code exposed
- No API keys or secrets
- No database schemas
- No business logic

✅ **Only these files are public:**
- index.html
- privacy-policy.html
- terms-of-service.html
- accessibility.html
- styles.css
- README.md
- .gitignore

---

## 📧 Support

Questions? Contact:
- **Privacy**: privacy@streetzone.app
- **Legal**: legal@streetzone.app
- **Accessibility**: accessibility@streetzone.app

**Last Updated**: October 19, 2025
