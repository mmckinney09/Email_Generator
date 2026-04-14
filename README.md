# 🔧 Chromebook Repair Email Generator

A lightweight, zero-dependency HTML tool designed to automate and standardize Chromebook repair notification emails for school IT departments.

## ✨ Features
- 🌙 **Dark Mode UI** with district-branded accent colors (`#9a2234` Red & `#feda15` Gold)
- 📧 **Auto-CC Routing** based on student grade and team (secretaries, team leaders, counselors)
- 👨‍👩‍👧 **Multi-Parent Support** with automatic greeting generation
- 📋 **One-Click Clipboard** for instant pasting into Outlook, Teams, or Gmail
- 🌐 **100% Offline** - No servers, APIs, or installations required. Runs locally in any modern browser.

## 🚀 Quick Start
1. Download or clone this repository.
2. Open `Chromebook_Email_Generator.html` (or rename to `index.html` for GitHub Pages) in any web browser.
3. Open the file in a text editor and update the `CONFIG` object with your district's actual email addresses.
4. Fill out the form, click **Generate Email**, then **Copy to Clipboard**.
5. Paste directly into your email client and send.

## ⚙️ Configuration
Locate the `const CONFIG = { ... }` block near the bottom of the HTML file and update it with your school's routing logic:
```javascript
const CONFIG = {
  secretaries: ["sec1@district.edu", "sec2@district.edu"],
  counselors: { 
    "6": "counselor6@district.edu", 
    "7": "counselor7@district.edu", 
    "8": "counselor8@district.edu" 
  },
  teamLeaders: {
    "6": { "1": "team6-1@district.edu", "2": "team6-2@district.edu", "3": "team6-3@district.edu" },
    "7": { "1": "team7-1@district.edu", "2": "team7-2@district.edu", "3": "team7-3@district.edu" },
    "8": { "1": "team8-1@district.edu", "2": "team8-2@district.edu", "3": "team8-3@district.edu" }
  }
};
```
