# JAEN Changelog

## Version 2.1.0 (2025-08-28 - Recovery 2025-08-31)

### 🚀 New Features
- **URL Summary Feature**: Automatically extracts and summarizes webpage content
  - Extracts meta tags: title, description, author, keywords
  - Displays in both Japanese and English
  - Uses cheerio for HTML parsing
  - Fallback error handling
- Enhanced user experience with formatted output
- Maintained backward compatibility with translation features

### 🔧 Recovery Updates (2025-08-31)
- **Critical Fix**: Added missing "start" script in package.json
- Added "dev" script for development convenience
- Created comprehensive troubleshooting documentation
- Updated README with npm start instructions across 3 languages

### 🛠️ Technical Changes
- Added cheerio dependency for HTML parsing
- Implemented extractPageMetadata() function
- Added URL detection logic with isUrl() function
- Created bilingual summary formatting
- Added comprehensive error handling for web requests
- Fixed package.json scripts section for proper npm start functionality

### 📁 Files Modified
- `index.js`: Added URL summary functionality (80 lines of new code)
- `package.json`: Added cheerio dependency, fixed scripts, updated version
- `README.md`: Updated documentation for v2.1.0 features and npm start (3 languages)
- `docs/TROUBLESHOOTING.md`: **NEW** - Comprehensive recovery guide
- `CHANGELOG.md`: **NEW** - This changelog file

### 🎯 Migration Guide
```bash
# For existing installations
npm install cheerio
npm start  # Now works properly
```

---

## Version 2.0.1 (2025-08-28)

### 🔧 Bug Fixes
- **Format Preservation**: Maintains line breaks and Discord markdown in translations
- **Markdown Support**: Preserves bold, italic, code, strikethrough, underline formatting
- Enhanced translation quality with structure preservation

### 🛠️ Technical Changes  
- Implemented parseMarkdownStructure() function
- Added translateWithFormatting() function
- Added getMarkdownWrapper() helper
- Fallback mechanism for complex formatting

### 📁 Files Modified
- `index.js`: Added format preservation logic (114 lines)
- `package.json`: Updated to v2.0.1
- `README.md`: Updated documentation

---

## Version 2.0.0 (2025-08-27)

### 🚀 Major Release
- **Enhanced Japanese Detection**: Allows English words within Japanese sentences  
- **Smart Language Logic**: Differentiates Japanese text vs English grammar structures
- **Improved Accuracy**: Better handling of mixed-language content

### 🛠️ Technical Changes
- Completely rewritten isJapaneseMain() function
- Added English sentence pattern detection
- Improved Japanese character ratio calculation (40% threshold)
- Enhanced noise filtering

### 📁 Files Modified
- `index.js`: Major refactor of language detection logic
- `package.json`: Updated to v2.0.0
- `README.md`: Updated documentation with examples

---

## Version 1.0.0 (2025-08-27)

### 🎉 Initial Release
- **Core Translation**: Japanese to English automatic translation
- **Discord Integration**: Full discord.js v14 support
- **Google Translation API**: High-quality translations
- **Channel Filtering**: Configurable channel restrictions
- **Smart Filtering**: Ignores bots, code blocks, URLs, images

### 🛠️ Technical Stack
- Node.js + discord.js v14
- Google Cloud Translation API  
- Environment-based configuration
- Comprehensive logging

### 📁 Initial Files
- `index.js`: Core bot functionality
- `package.json`: Project configuration
- `.env.template`: Environment template
- `README.md`: Initial documentation
- `.gitignore`: Git configuration

---

*Maintained by: Claude + peaske*  
*Repository: https://github.com/AXSC-Studio/jaen*
