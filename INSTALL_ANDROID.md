# FTN mStudent - Android Installation Guide

## Method 1: Install as PWA (Progressive Web App) - RECOMMENDED

This is the easiest way to install the app on your Android phone:

### Steps:

1. **Upload all files to a web server:**
   - student-portal.html
   - manifest.json
   - service-worker.js
   - (Optional) icon-192.png and icon-512.png

2. **Open in Chrome on your Android phone:**
   - Navigate to the URL where you uploaded the files
   - Example: `https://your-domain.com/student-portal.html`

3. **Install the app:**
   - Tap the **three dots menu** (⋮) in Chrome
   - Select **"Add to Home screen"** or **"Install app"**
   - Confirm the installation
   - The app will appear on your home screen like a native app!

### Benefits:
- ✅ Launches fullscreen without browser UI
- ✅ Has its own icon on home screen
- ✅ Works offline after first load
- ✅ Looks and feels like a native app
- ✅ No app store required
- ✅ Updates automatically

---

## Method 2: Use Directly in Browser

If you don't want to install:

1. Download `student-portal.html` to your phone
2. Open it with Chrome, Firefox, or Samsung Internet
3. Add bookmark to home screen for quick access

---

## Method 3: Create APK with Capacitor (Advanced)

For developers who want a real APK file:

### Requirements:
- Node.js installed
- Android Studio installed
- Java JDK installed

### Steps:

```bash
# Install Capacitor CLI
npm install -g @capacitor/cli

# Create new Capacitor project
npm init @capacitor/app

# Install Android platform
npm install @capacitor/android

# Add Android platform
npx cap add android

# Copy your student-portal.html to www folder
cp student-portal.html www/index.html
cp manifest.json www/
cp service-worker.js www/

# Sync files
npx cap sync

# Open in Android Studio
npx cap open android

# Build APK in Android Studio:
# Build > Build Bundle(s) / APK(s) > Build APK(s)
```

---

## Creating App Icons (Optional but Recommended)

You'll need two icon sizes:
- **192x192 pixels** - saved as `icon-192.png`
- **512x512 pixels** - saved as `icon-512.png`

Use any image editor to create a square icon with the FTN logo or student portal design.

Online tools:
- https://realfavicongenerator.net/
- https://www.favicon-generator.org/

---

## Troubleshooting

**App won't install:**
- Make sure you're using HTTPS (not HTTP)
- Check that manifest.json is in the same folder
- Clear Chrome cache and try again

**Offline mode not working:**
- Ensure service-worker.js is in the same folder
- Check browser console for errors
- Try accessing the app online first

**Icons not showing:**
- Create icon-192.png and icon-512.png
- Update manifest.json with correct paths
- Reinstall the app

---

## Quick Host Options

If you don't have a web server:

1. **GitHub Pages** (Free):
   - Create GitHub repository
   - Upload files
   - Enable GitHub Pages
   - Access at `https://username.github.io/repo-name/student-portal.html`

2. **Netlify** (Free):
   - Drag and drop folder to netlify.com
   - Get instant HTTPS URL

3. **Vercel** (Free):
   - Import project from GitHub
   - Automatic deployment

---

## Notes

- The app works best in **portrait mode** on phones
- Designed for **480px max width** (mobile screens)
- All data is stored locally in browser
- No backend server required
- Works completely offline after first load

---

For questions or issues, contact FTN IT support.
