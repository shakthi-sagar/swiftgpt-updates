# SwiftGPT Updates

This repository contains the update feed for SwiftGPT, served via GitHub Pages and GitHub Releases.

## 🚀 Automatic Release Process

### How it works:
1. **Generate release** using the build script in SwiftGPT project
2. **Copy files** to this repository:
   - `SwiftGPT-{version}.dmg` 
   - `appcast.xml`
3. **Commit and push** the files
4. **Create and push a tag** to trigger release:
   ```bash
   git add .
   git commit -m "Release v1.1"
   git tag v1.1
   git push origin main
   git push origin v1.1
   ```

### What happens automatically:
- ✅ **GitHub Actions** creates a GitHub Release
- ✅ **DMG file** gets uploaded to the release
- ✅ **GitHub Pages** serves the updated `appcast.xml`
- ✅ **Sparkle** can now download the update

## 📁 Files

- `appcast.xml` - Sparkle update feed (auto-served via GitHub Pages)
- `SwiftGPT-{version}.dmg` - App installer (uploaded to GitHub Releases)
- `.github/workflows/create-release.yml` - Automation workflow

## 🔗 URLs

- **Appcast**: https://shakthi-sagar.github.io/swiftgpt-updates/appcast.xml
- **Releases**: https://github.com/shakthi-sagar/SwiftGPT/releases
- **Main App**: https://github.com/shakthi-sagar/SwiftGPT

## 🧪 Testing

To test the update system:
1. Lower your app version to an older number (e.g., 1.0)
2. Build and run the app
3. The app should automatically detect and offer the newer version

## 📋 Release Checklist

- [ ] Generate release files with build script
- [ ] Copy DMG and appcast.xml to this repo
- [ ] Commit changes
- [ ] Create and push version tag (e.g., `v1.1`)
- [ ] Verify GitHub Release was created
- [ ] Test update in app
