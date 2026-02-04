# VitaTrack PWA - Installation Guide

This is a Progressive Web App (PWA) that can be installed on your Android device via Brave browser.

## Requirements for PWA Installation

PWAs **must be served over HTTPS** to be installable. Opening the HTML file directly from your phone's storage (file://) won't work.

## Easy Free Hosting Options

### Option 1: GitHub Pages (Recommended)
1. Create a free GitHub account at github.com
2. Create a new repository (e.g., "vitatrack")
3. Upload all files from this zip (index.html, manifest.json, sw.js, icons folder)
4. Go to Settings → Pages → Source: "main" branch → Save
5. Your app will be at: `https://yourusername.github.io/vitatrack/`

### Option 2: Netlify Drop (Easiest)
1. Go to https://app.netlify.com/drop
2. Drag and drop the entire `vitatrack-pwa` folder
3. You'll get a URL like `https://random-name.netlify.app`
4. (Optional) Create a free account to keep the site permanently

### Option 3: Vercel
1. Go to https://vercel.com
2. Sign up with GitHub
3. Import your repository or drag-drop files
4. Get a free HTTPS URL

### Option 4: Cloudflare Pages
1. Go to https://pages.cloudflare.com
2. Connect GitHub or upload directly
3. Get a free HTTPS URL

## Installing on Brave Android

Once hosted on HTTPS:

1. Open your hosted URL in Brave browser on Android
2. Wait a few seconds for the page to load
3. You should see an "Install" banner at the top, OR
4. Tap the menu (⋮) → "Install app" or "Add to Home screen"
5. Confirm the installation
6. VitaTrack will appear on your home screen!

## What's Changed from Original

- Removed meal type selection (breakfast/lunch/dinner/snack)
- Meals now just record the timestamp when you ate
- Added PWA manifest and service worker for installability
- Added proper icons (192px and 512px)

## Files Included

```
vitatrack-pwa/
├── index.html      # Main app
├── manifest.json   # PWA manifest (required)
├── sw.js           # Service worker (for offline support)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Troubleshooting

**"Install" option not showing?**
- Make sure you're on HTTPS (not http://)
- Clear browser cache and reload
- Wait a few seconds after page loads
- Check if service worker registered (DevTools → Application → Service Workers)

**App not working offline?**
- The service worker needs to cache files first
- Visit the app once while online, then it should work offline
