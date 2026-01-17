# Deployment Guide - Portfolio Website

## Quick Start Guide for GitHub Pages

### Step 1: Prepare Your Repository

1. Create a new repository on GitHub named `username.github.io` (replace `username` with your actual GitHub username)
   - Example: `jupiterseho.github.io`

2. Clone this portfolio locally if you haven't already

### Step 2: Push to GitHub

```bash
# Navigate to portfolio directory
cd portfolio

# Initialize git (if not already done)
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial portfolio commit"

# Add remote origin (replace USERNAME with your GitHub username)
git remote add origin https://github.com/USERNAME/USERNAME.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Configure GitHub Pages

1. Go to your GitHub repository settings
2. Scroll down to "Pages" section
3. Make sure "Source" is set to "Deploy from a branch"
4. Select "main" branch and "/" (root) folder
5. Click "Save"

### Step 4: Verify Deployment

1. After a few minutes, your site will be live at: `https://USERNAME.github.io`
2. Check the "Pages" section in Settings for the live URL
3. You should see a green checkmark when deployment is successful

---

## Custom Domain Setup (Optional)

If you have a custom domain (e.g., `portfolio.yourdomain.com`):

1. Update the `CNAME` file with your domain:
```
portfolio.yourdomain.com
```

2. Commit and push the changes:
```bash
git add CNAME
git commit -m "Add custom domain"
git push origin main
```

3. In your domain registrar settings, create a `CNAME` record:
   - **Name**: `portfolio` (or `www`)
   - **Target**: `USERNAME.github.io`
   - **TTL**: 3600 (or default)

4. Wait for DNS propagation (can take up to 48 hours)

5. In GitHub repository Settings → Pages, enter your custom domain

---

## Updating Your Portfolio

To update content:

1. Make changes to `index.html`, `css/styles.css`, or `js/script.js`
2. Test locally by opening `index.html` in your browser
3. Commit and push changes:
```bash
git add .
git commit -m "Update portfolio content"
git push origin main
```

4. GitHub Pages will automatically rebuild and deploy (usually within 1-2 minutes)

---

## Troubleshooting

### Site not showing up
- Wait a few minutes for GitHub to build and deploy
- Check the Pages settings in your repository
- Ensure files are in the root directory or `/docs` folder

### Custom domain not working
- Check DNS records are correctly configured
- Ensure CNAME file has your domain without `https://`
- Wait for DNS propagation (can take up to 48 hours)

### Changes not appearing
- Clear your browser cache (Ctrl+F5 or Cmd+Shift+R)
- Check that you pushed to the correct branch
- Verify the deployment status in GitHub Pages settings

### 404 error
- Ensure `index.html` is in the root directory
- Check that all file paths in HTML are correct (relative paths)

---

## Performance Tips

1. **Optimize Images** (when adding):
   - Use WebP or optimized PNG/JPG
   - Compress before uploading
   - Use appropriate dimensions

2. **Caching**:
   - GitHub Pages sets proper cache headers automatically
   - Browser caching helps on repeat visits

3. **Monitoring**:
   - Use Google Analytics to track visitors
   - Monitor performance with Lighthouse

---

## Best Practices

- Keep content updated regularly
- Test locally before pushing
- Use meaningful commit messages
- Backup your local copy
- Monitor GitHub for security alerts

---

## Additional Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Pages Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-publication-of-your-github-pages-site)
- [Custom Domain Guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

---

## Need Help?

If you encounter issues:
1. Check GitHub Pages documentation
2. Review GitHub Actions logs for build errors
3. Verify file permissions and paths
4. Contact GitHub support if needed

Happy hosting! 🚀
