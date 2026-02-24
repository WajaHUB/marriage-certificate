# GitHub Pages Setup Instructions

Follow these steps to deploy your marriage certificate generator to GitHub Pages.

## Prerequisites

1. **GitHub Account** - Create one at [github.com](https://github.com) if you don't have one
2. **Git installed** - Download from [git-scm.com](https://git-scm.com/) if not already installed

## Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right, then "New repository"
3. Name your repository (e.g., "marriage-certificate")
4. Make it **Public** (required for free GitHub Pages)
5. Don't initialize with README, .gitignore, or license (we already have files)
6. Click "Create repository"

## Step 2: Upload Your Files

### Option A: Using Git Command Line

1. Open Command Prompt or PowerShell
2. Navigate to your project folder:
   ```
   cd "C:\Users\jackf\OneDrive\Desktop\marriage-certificate"
   ```

3. Initialize git repository:
   ```
   git init
   git add .
   git commit -m "Initial commit: Marriage certificate generator"
   ```

4. Connect to GitHub (replace YOUR_USERNAME and YOUR_REPO):
   ```
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
   git branch -M main
   git push -u origin main
   ```

### Option B: Using GitHub Web Interface

1. On your GitHub repository page, click "uploading an existing file"
2. Drag and drop all files from your project folder:
   - `index.html`
   - `certificate.png.jpeg`
   - `README.md`
   - `.gitignore`
   - `SETUP.md`
3. Add commit message: "Initial commit: Marriage certificate generator"
4. Click "Commit changes"

## Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click "Settings" tab
3. Scroll down to "Pages" in the left sidebar
4. Under "Source", select "Deploy from a branch"
5. Choose "main" branch
6. Select "/ (root)" folder
7. Click "Save"

## Step 4: Access Your Site

Your site will be available at:
```
https://YOUR_USERNAME.github.io/YOUR_REPOSITORY_NAME
```

**Note**: It may take a few minutes for GitHub Pages to build and deploy your site.

## Step 5: Customize Your Certificate

1. **Replace the certificate image**:
   - Replace `certificate.png.jpeg` with your own certificate template
   - Use high resolution for best PDF quality
   - Recommended dimensions: 8.5" × 11" aspect ratio

2. **Adjust text positioning**:
   - Open `index.html` in a text editor
   - Find the CSS classes (around line 132-161):
     - `.groom-name { top: 300px; left: 150px; }`
     - `.bride-name { top: 300px; right: 150px; }`
     - `.mahr-amount { top: 400px; left: 150px; }`
     - `.ceremony-date { top: 400px; right: 150px; }`
     - `.imam-name { bottom: 150px; left: 50%; }`
   - Adjust the `top`, `bottom`, `left`, `right` values to match your certificate layout
   - Save and push changes to GitHub

3. **Test positioning**:
   - Visit your GitHub Pages site
   - Generate a test certificate
   - If text positioning is off, adjust the CSS values and push again

## Step 6: Update Repository Information

1. Edit `README.md` and replace:
   - `https://yourusername.github.io/marriage-certificate` with your actual URL
   - Update any other placeholder information

2. Commit and push your changes

## Troubleshooting

### Site Not Loading
- Wait 5-10 minutes after enabling GitHub Pages
- Check that your repository is public
- Verify GitHub Pages settings

### Certificate Image Not Showing
- Ensure `certificate.png.jpeg` is in the root directory
- Check the filename exactly matches what's in `index.html` line 105
- Make sure the image file was uploaded correctly

### Text Positioning Issues
- Use browser developer tools (F12) to inspect elements
- Adjust CSS positioning values incrementally
- Test with different screen sizes

### PDF Generation Problems
- Ensure stable internet connection (html2pdf.js loads from CDN)
- Try different browsers (Chrome/Edge recommended)
- Check browser console for JavaScript errors

## Making Updates

To update your site:
1. Make changes to your local files
2. Commit and push to GitHub:
   ```
   git add .
   git commit -m "Description of changes"
   git push
   ```
3. GitHub Pages will automatically rebuild your site

## Custom Domain (Optional)

To use your own domain:
1. Add a `CNAME` file to your repository with your domain
2. Configure DNS settings with your domain provider
3. Update GitHub Pages settings

## Security Note

This application processes all data client-side in the browser. No information is sent to any server, ensuring privacy and security of personal information.