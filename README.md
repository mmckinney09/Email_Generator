# 🔧 Chromebook Repair Email Generator

A lightweight, zero-dependency HTML tool that automates and standardizes Chromebook repair notification emails for school IT departments. Built to replace repetitive copy-pasting, ensure accurate staff/parent routing, and maintain consistent district communication.

## ✨ Features
- 🌗 **Persistent Dark/Light Mode** – Toggle fixed to the top-right, preference saved via `localStorage`
- 📤 **One-Click Gmail Integration** – Opens a pre-filled compose window (`To`, `CC`, `Subject`, `Body`)
- 🏫 **Smart Auto-CC Routing** – Dynamically routes emails based on student grade & team (secretaries, team leaders, counselors)
- 💰 **Flexible Fee Selector** – Dropdown for `$25.00`, `$80.00`, or custom amount (auto-formats to `$XX.XX`)
- 🔩 **Multi-Part Selector** – Tag-style checkboxes for standard Chromebook components + custom "Other" field
- 📋 **Granular Copy Controls** – Copy individual fields or the entire email payload instantly
- 🌐 **100% Offline & Zero Dependencies** – No servers, APIs, frameworks, or installations required. Runs locally in any modern browser.

## 🚀 Quick Start
1. Download or clone this repository.
2. Open `Chromebook_Email_Generator.html` in any web browser (Chrome, Edge, Firefox, Safari).
3. Open the file in a text editor and update the `CONFIG` object with your district's actual email addresses.
4. Fill out the form → click **📤 Open in Gmail** → review → send.

## ⚙️ Configuration
Locate the `const CONFIG = { ... }` block in the `<script>` section and update it to match your school's routing logic:
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
