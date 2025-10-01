# GitHub Repository Setup Instructions

## Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Fill in the details:
   - **Repository name**: `prizo-extension`
   - **Description**: `🏷️ Prizo - دستیار قیمت‌یابی دیجی‌کالا | Digikala Price Tracking Extension for Chrome & Firefox`
   - **Visibility**: Public
   - **Do NOT initialize with**: README, .gitignore, or license (we already have these)
5. Click "Create repository"

## Step 2: Connect Local Repository to GitHub

After creating the repository on GitHub, you'll see setup instructions. Use these commands:

```bash
cd /d/python/Release/prizo-extension

# Add the remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/prizo-extension.git

# Rename branch to main (if needed)
git branch -M main

# Push to GitHub
git push -u origin main
```

## Step 3: Configure Repository Settings

1. Go to your repository on GitHub
2. Click "Settings" → "General"
3. Scroll to "Features" section:
   - ✅ Enable "Issues" (for bug reports and feature requests)
   - ✅ Enable "Discussions" (optional, for community discussions)
   - ❌ Disable "Wikis" (not needed)
   - ❌ Disable "Projects" (optional)

## Step 4: Create First GitHub Release

1. Go to your repository on GitHub
2. Click "Releases" (right sidebar)
3. Click "Create a new release"
4. Fill in the details:
   - **Tag version**: `v4.2.6`
   - **Release title**: `v4.2.6 - Initial Public Release`
   - **Description**: Copy from CHANGELOG.md for version 4.2.6
5. Upload the zip file: `releases/prizo-v4.2.6.zip`
6. Check "Set as the latest release"
7. Click "Publish release"

## Step 5: Add Topics/Tags

1. Go to your repository homepage
2. Click the gear icon ⚙️ next to "About"
3. Add these topics:
   - `chrome-extension`
   - `firefox-addon`
   - `digikala`
   - `price-tracker`
   - `persian`
   - `farsi`
   - `e-commerce`
   - `browser-extension`
   - `price-history`
   - `price-comparison`

## Step 6: Update README Links

After creating the repository, update these placeholders in README.md:
- Replace `YOUR_USERNAME` with your actual GitHub username
- Update donation links if you have them
- Add your actual email address
- Add screenshot images to an `images/` or `screenshots/` folder

## Step 7: Set Up Issue Templates (Optional)

Create `.github/ISSUE_TEMPLATE/` directory with templates for:
- Bug reports
- Feature requests
- Questions

## Step 8: Add Repository Description and Website

1. Click the gear icon ⚙️ next to "About" on your repository page
2. Add description: `🏷️ Prizo - دستیار قیمت‌یابی دیجی‌کالا | Digikala Price Tracking Extension`
3. Add website URL (if you have one)
4. Add topics (as mentioned in Step 5)
5. Click "Save changes"

## Repository Structure

```
prizo-extension/
├── .gitignore
├── LICENSE
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SETUP_INSTRUCTIONS.md (this file - can be deleted after setup)
└── releases/
    ├── README.md
    └── prizo-v4.2.6.zip
```

## Future Updates

When releasing new versions:

1. Build the new version in your development repository
2. Package it as a zip file
3. Add it to the `releases/` folder
4. Update `CHANGELOG.md`
5. Commit and push changes
6. Create a new GitHub Release with the new zip file

## Automation (Optional)

Consider setting up GitHub Actions to:
- Automatically create releases when you push version tags
- Validate extension structure
- Run automated checks

---

**Note**: After completing the setup, you can delete this file or keep it for reference.
