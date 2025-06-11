# Unsplash Instant

🖼️ Beautiful photos from [Unsplash](https://unsplash.com) in your new Chrome tabs.

## ⚠️ Important Notice

**This is a backup/archive of the Unsplash Instant Chrome extension that is no longer available in the Chrome Web Store.** A Manifest V3 rewrite is currently in progress to modernize the extension and ensure compatibility with current Chrome standards.

## Overview

Unsplash Instant was a Chrome extension that replaced your new tab page with stunning photography from Unsplash. Each time you opened a new tab, you were greeted with a high-quality, curated photograph along with photographer information and EXIF data.

## Features

### 🎨 **Beautiful Photography**
- High-resolution photos from Unsplash's curated collection
- New photo every time you open a tab
- Optimized image loading based on screen resolution

### 📸 **Photo Information**
- Photographer name and profile link
- Photo location (when available)
- Complete EXIF data (camera, lens, settings)
- Publication date and photo dimensions

### 🔧 **Customization Options**
- **Motion Effects**: Enable/disable photo transition animations
- **Minimal UI**: Hide interface elements for distraction-free viewing
- **Photo History**: View previously shown photos
- **Download**: Save photos directly to your computer

### 🚀 **Quick Actions**
- One-click photo downloads
- Share photos on Facebook and Twitter
- View full photo details on Unsplash
- Access Chrome Apps page
- Return to default new tab

### 📱 **Responsive Design**
- Adapts to different screen sizes
- Optimized for both desktop and laptop displays
- Clean, modern interface that doesn't distract from the photography

## Status & Installation

### Current Status
- **Original Extension**: No longer available in Chrome Web Store
- **This Repository**: Backup/archive of the original Manifest V2 version
- **Active Development**: Manifest V3 rewrite in progress

### Development Installation (Manifest V2 Legacy)
⚠️ **Note**: This legacy version may not work properly in newer Chrome versions due to Manifest V2 deprecation.

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/unsplash-instant.git
   cd unsplash-instant
   ```

2. Open Chrome and navigate to `chrome://extensions/`

3. Enable "Developer mode" (toggle in top right)

4. Click "Load unpacked" and select the project directory

5. The extension will attempt to override your new tab page

### Manifest V3 Version
🚧 **Coming Soon**: A fully rewritten Manifest V3 version is under development that will:
- Be compatible with current Chrome extension standards
- Remove deprecated Google Analytics integration
- Implement modern service worker architecture
- Maintain all original functionality

## Development

### Project Structure (Current - Manifest V2)
```
unsplash-instant/
├── manifest.json          # Extension configuration (V2)
├── index.html             # New tab page template
├── js/
│   ├── main.js           # Frontend logic (minified)
│   └── background.js     # Background scripts (minified)
├── css/
│   └── main.css          # Styles
├── img/
│   └── icons/            # Extension icons
└── _locales/
    └── en/               # Localization files
```

### Key Components

**manifest.json**
- Extension metadata and permissions
- **Currently Manifest V2** (legacy/deprecated)
- Overrides new tab page with `index.html`

**index.html**
- Single-page application structure
- Photo display container
- UI controls and settings panels
- EXIF data popover

**JavaScript Files**
- `main.js`: Frontend functionality, UI interactions, photo management
- `background.js`: Background tasks, API calls, photo prefetching

### Features Implementation

**Photo Management**
- Fetches random photos from Unsplash API
- Caches next photo for instant loading
- Maintains photo history in localStorage
- Handles image optimization and base64 conversion

**UI Controls**
- Click tracking for analytics (to be removed in V3)
- Popover menus for settings and info
- Responsive design with CSS classes
- Animation toggles and minimal UI mode

**Settings Persistence**
- Uses localStorage for user preferences
- Remembers animation and UI settings
- Maintains photo history between sessions

## API Integration

The extension integrates with the Unsplash API to fetch photos:

- **Endpoint**: `https://api.unsplash.com/photos/random`
- **Collection**: Uses curated collection ID `317099`
- **Orientation**: Landscape photos only
- **Client ID**: Configured for Unsplash API access

### API Features Used
- Random photo fetching
- Download tracking
- Photographer information
- EXIF data retrieval
- Location data (when available)

## Browser Compatibility

- **Chrome**: Originally designed for Chrome (Manifest V2 - now deprecated)
- **Current Status**: May not work in newer Chrome versions
- **Future**: Manifest V3 version will restore full compatibility

## Manifest V3 Migration (In Progress)

🚧 **Active Development**: This extension is being completely rewritten for Manifest V3 compatibility.

### Migration Goals
1. ✅ Update `manifest_version` to 3
2. 🚧 Replace background scripts with service workers
3. 🚧 Update content security policy format
4. ✅ Remove Google Analytics integration (privacy improvement)
5. 🚧 Update API calls to use modern Chrome extension APIs
6. 🚧 Implement proper error handling and fallbacks
7. 🚧 Add automated testing

### Why the Migration is Necessary
- **Manifest V2 Deprecation**: Google deprecated Manifest V2 in 2023
- **Store Requirements**: Chrome Web Store now requires Manifest V3
- **Security Improvements**: V3 provides better security and performance
- **Future-Proofing**: Ensures long-term compatibility

### Migration Progress
- [ ] Service worker implementation
- [ ] CSP updates for extension_pages
- [ ] Background script conversion
- [ ] API call modernization
- [ ] Testing framework setup
- [ ] Chrome Web Store resubmission

## Contributing

### Current Priorities
1. **Manifest V3 Migration**: Help complete the rewrite
2. **Testing**: Ensure all features work in the new version
3. **Documentation**: Update for V3 architecture
4. **Privacy**: Remove remaining analytics code

### Getting Started
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/v3-migration`
3. Focus on Manifest V3 compatibility
4. Test thoroughly with latest Chrome versions
5. Submit a pull request

### Development Guidelines
- **Target Manifest V3** for all new development
- Follow modern Chrome extension best practices
- Prioritize privacy (no analytics/tracking)
- Maintain existing user experience
- Ensure responsive design across devices

## Privacy & Analytics

### Legacy Version (This Repository)
- Contains Google Analytics tracking (deprecated)
- Will be completely removed in Manifest V3 version

### Future Version
- **No tracking or analytics** - privacy-first approach
- Local storage only for user preferences
- No data transmission except Unsplash API calls
- Full transparency in data usage

## Project History

### Timeline
- **Original Release**: Available in Chrome Web Store
- **Discontinuation**: Removed from store (Manifest V2 deprecation)
- **Archive**: This repository preserves the original code
- **Current**: Manifest V3 rewrite in active development
- **Future**: Planned resubmission to Chrome Web Store

### Why It Was Removed
- Manifest V2 deprecation by Google
- Required complete architectural rewrite
- Temporary removal during migration period

## License

This project appears to be related to Unsplash. Please ensure compliance with:
- [Unsplash API Terms](https://unsplash.com/api-terms)
- [Unsplash License](https://unsplash.com/license)
- Chrome Web Store Developer Policies

## Support

### For This Archive Version
- This is a legacy backup - limited support available
- Known issues with newer Chrome versions expected

### For Future Manifest V3 Version
- GitHub issues for the rewritten version
- Full support planned upon completion
- Community contributions welcome

## Acknowledgments

- **Unsplash**: For providing the beautiful photography API
- **Chrome Extension Team**: For the extension platform
- **Community**: For preserving and updating this beloved extension
- **Contributors**: Thanks to all working on the Manifest V3 migration

---

**🔄 Currently being rewritten for Manifest V3 - Stay tuned for the modern version!** 