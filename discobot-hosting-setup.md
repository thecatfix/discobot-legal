# DiscoBot Legal Pages Hosting Setup

## Option 1: GitHub Pages (Recommended - Free & Easy)

### Steps:
1. Create new GitHub repository: `discobot-legal`
2. Upload both HTML files to the repository
3. Enable GitHub Pages in repository settings
4. Your URLs will be:
   - `https://yourusername.github.io/discobot-legal/discobot-terms-of-service.html`
   - `https://yourusername.github.io/discobot-legal/discobot-privacy-policy.html`

### Quick Commands:
```bash
# Create and setup repository
mkdir discobot-legal
cd discobot-legal
cp ~/discobot-*.html .
git init
git add .
git commit -m "Add DiscoBot legal pages"
git remote add origin https://github.com/yourusername/discobot-legal.git
git push -u origin main
```

## Option 2: Netlify Drop (Alternative - Also Free)

### Steps:
1. Go to [netlify.com/drop](https://netlify.com/drop)
2. Drag both HTML files to the drop zone
3. Get instant hosting URLs
4. Optional: Customize domain name

## Option 3: Simple HTTP Server (Testing Only)

### For local testing:
```bash
cd ~/
python3 -m http.server 8000
# Access at: http://localhost:8000/discobot-terms-of-service.html
```

## Recommended: GitHub Pages Setup

1. Go to GitHub.com and create new repository: `discobot-legal`
2. Clone repository locally
3. Copy HTML files to repository
4. Push to GitHub
5. Enable Pages in repository Settings > Pages
6. Use URLs in Discord Developer Portal

## Files Created:
- `/Users/johnshelburne/discobot-terms-of-service.html`
- `/Users/johnshelburne/discobot-privacy-policy.html`

Ready to upload to your chosen hosting platform!