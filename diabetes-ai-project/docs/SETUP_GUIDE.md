# Setup Guide for AI Diabetes Risk Intelligence System

This guide will walk you through setting up the project on your local machine and deploying it to GitHub Pages.

## Table of Contents

1. [Local Development Setup](#local-development-setup)
2. [GitHub Repository Setup](#github-repository-setup)
3. [GitHub Pages Deployment](#github-pages-deployment)
4. [Customization Guide](#customization-guide)
5. [Troubleshooting](#troubleshooting)

## Local Development Setup

### Step 1: Download the Project

If you received the project files:

```bash
# Extract the zip file (if applicable)
unzip diabetes-ai-system.zip
cd diabetes-ai-system
```

### Step 2: Open in Browser

The simplest way:

```bash
# Just double-click index.html
# Or use your browser's File > Open option
```

### Step 3: Use a Local Server (Recommended)

For better development experience:

**Option A: Python (if installed)**
```bash
# Python 3
python -m http.server 8000

# Python 2 (older systems)
python -m SimpleHTTPServer 8000
```

**Option B: Node.js (if installed)**
```bash
# Using npx (no installation needed)
npx http-server

# Or install globally
npm install -g http-server
http-server
```

**Option C: VS Code Live Server**
1. Install "Live Server" extension in VS Code
2. Right-click `index.html`
3. Select "Open with Live Server"

Then visit: `http://localhost:8000`

## GitHub Repository Setup

### Step 1: Create a GitHub Account

If you don't have one: [Sign up at GitHub](https://github.com/join)

### Step 2: Create a New Repository

1. Go to [GitHub](https://github.com)
2. Click the "+" icon in the top right
3. Select "New repository"
4. Fill in the details:
   - **Repository name**: `diabetes-ai-system` (or your preferred name)
   - **Description**: "AI-powered diabetes risk prediction system with interactive dashboard"
   - **Public** or **Private**: Choose based on your preference
   - **DO NOT** initialize with README (we already have one)

5. Click "Create repository"

### Step 3: Initialize Git in Your Project

Open terminal/command prompt in your project folder:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Make your first commit
git commit -m "Initial commit: Add diabetes risk prediction system"

# Add your GitHub repository as remote
# Replace YOUR_USERNAME and YOUR_REPO with your actual details
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 4: Personalize the Project

Before pushing, make these changes to make it yours:

**1. Update README.md**
```markdown
Replace:
- [Your Name] → Your actual name
- [@yourusername] → Your GitHub username
- [your.email@example.com] → Your email
- [Your LinkedIn] → Your LinkedIn profile URL
- [yourwebsite.com] → Your portfolio website
```

**2. Update LICENSE**
```
Replace [Your Name] with your actual name
```

**3. Add a profile section in index.html** (optional):
```html
<!-- Add this in the sidebar after model accuracy -->
<div style="margin-top: 1rem; padding-top: 1rem; border-top: 1px solid var(--border);">
  <p style="font-size: 0.75rem; color: var(--text-secondary);">
    Developed by<br>
    <strong style="color: var(--accent);">Your Name</strong>
  </p>
</div>
```

### Step 5: Regular Git Workflow

After making changes:

```bash
# Check what changed
git status

# Add files
git add .

# Commit with a message
git commit -m "feat: add new feature"

# Push to GitHub
git push
```

## GitHub Pages Deployment

Deploy your project for free on GitHub Pages!

### Method 1: Using GitHub Interface

1. Go to your repository on GitHub
2. Click "Settings"
3. Scroll to "Pages" in the left sidebar
4. Under "Source", select "main" branch
5. Click "Save"
6. Wait 1-2 minutes
7. Your site will be live at: `https://YOUR_USERNAME.github.io/YOUR_REPO/`

### Method 2: Using Command Line

```bash
# Make sure you're on main branch
git checkout main

# Ensure everything is committed
git add .
git commit -m "Deploy to GitHub Pages"
git push

# Then follow Method 1 steps 2-7
```

### Custom Domain (Optional)

If you have your own domain:

1. Add a `CNAME` file to your project:
   ```bash
   echo "yourdomain.com" > CNAME
   git add CNAME
   git commit -m "Add custom domain"
   git push
   ```

2. Configure DNS with your domain provider:
   - Add a CNAME record pointing to `YOUR_USERNAME.github.io`

3. In GitHub Pages settings, enter your custom domain

## Customization Guide

### Change Color Scheme

Edit the CSS variables in `index.html`:

```css
:root {
  --primary: #0A4D68;        /* Main brand color */
  --accent: #05C3DD;         /* Accent/highlight color */
  --success: #10B981;        /* Success/low risk */
  --warning: #F59E0B;        /* Warning/moderate risk */
  --danger: #EF4444;         /* Danger/high risk */
  /* ... other variables */
}
```

### Add Your Branding

Replace the emoji logo:

```html
<!-- Find this in the sidebar section -->
<div class="logo">🏥</div>

<!-- Replace with your logo image or different emoji -->
<div class="logo">
  <img src="your-logo.png" alt="Logo" style="width: 100%; height: 100%;">
</div>
```

### Modify the Model

The ML algorithm is in the JavaScript section:

```javascript
// Find this function
function predictDiabetes(features) {
  // Modify weights and thresholds here
  // to adjust the model behavior
}
```

### Add Google Analytics (Optional)

Add before `</head>`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## Troubleshooting

### Issue: Charts not displaying

**Solution**: Make sure you have internet connection (Chart.js loads from CDN)

### Issue: PDF download not working

**Solution**: Check browser console for errors. Try a different browser.

### Issue: GitHub Pages not updating

**Solution**: 
- Clear browser cache
- Wait 5-10 minutes for GitHub to rebuild
- Check GitHub Actions tab for build status
- Ensure index.html is in the root directory

### Issue: Predictions seem inaccurate

**Solution**: This is a demonstration model. For real medical use, a professionally trained and validated model would be needed.

### Issue: Git commands not working

**Solution**:
```bash
# Install git if not installed
# Windows: Download from git-scm.com
# Mac: Install Xcode Command Line Tools
xcode-select --install
# Linux:
sudo apt-get install git
```

### Issue: CORS errors when testing locally

**Solution**: Use a local server instead of opening the file directly. See [Local Development Setup](#step-3-use-a-local-server-recommended).

## Next Steps

1. ✅ Customize the project with your information
2. ✅ Test thoroughly in different browsers
3. ✅ Add screenshots to the README
4. ✅ Deploy to GitHub Pages
5. ✅ Share your project on LinkedIn, Twitter, etc.
6. ✅ Add it to your portfolio
7. ✅ Consider contributing improvements back to the community

## Getting Help

- **GitHub Issues**: Create an issue in your repository
- **Stack Overflow**: Tag your questions with `javascript`, `ml`, `healthcare`
- **GitHub Discussions**: Enable discussions in your repo settings

---

**Congratulations! Your project is now set up and ready to impress! 🎉**
