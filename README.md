# LinkedIn Job Filter & Analytics Pro

<p align="center">
  <a href="https://developer.chrome.com/docs/extensions/mv3/intro/"><img src="https://img.shields.io/badge/Manifest-V3-orange.svg?style=flat-square" alt="Manifest Version"></a>
  <a href="https://chrome.google.com/webstore"><img src="https://img.shields.io/badge/Chrome-Extension-4285F4.svg?style=flat-square&logo=google-chrome&logoColor=white" alt="Chrome Extension"></a>
  <img src="https://img.shields.io/badge/version-1.2.6-blue.svg?style=flat-square" alt="Version 1.2.6">
  <a href="../LICENSE"><img src="https://img.shields.io/badge/License-MIT%20%2B%20Indemnification-blue.svg?style=flat-square" alt="License: MIT with Indemnification Shield"></a>
  <img src="https://img.shields.io/badge/Pure-JavaScript%20(No%20Dependencies)-blueviolet.svg?style=flat-square" alt="Zero Dependencies">
  <img src="https://img.shields.io/badge/Privacy-100%25%20Local%20Processing-brightgreen.svg?style=flat-square" alt="100% Local">
</p>

A powerful, user-friendly Chrome extension designed to declutter, streamline, and supercharge your LinkedIn job search. Create custom keyword rules to auto-hide irrelevant listings, highlight top opportunities, surface hidden job insights (such as real applicant counts, salary ranges, experience requirements, and ghost job alerts) with a sleek floating widget, and effortlessly track your job applications — all processed **100% locally** in your browser with complete privacy.

---

## 📑 Table of Contents

- [✨ Why You'll Love It](#-why-youll-love-it)
- [🚀 Key Features](#-key-features)
  - [🔍 Smart Filtering & Custom Rules](#-smart-filtering--custom-rules)
  - [📝 Applied Jobs Tracker](#-applied-jobs-tracker)
  - [📊 Floating Job Insights Widget (HUD)](#-floating-job-insights-widget-hud)
  - [📈 Search Analytics & Activity Trends](#-search-analytics--activity-trends)
  - [🎨 Modern Design & Custom Themes](#-modern-design--custom-themes)
  - [⚙️ Settings, Presets & Data Portability](#️-settings-presets--data-portability)
  - [📋 Built-In Release Notes & Updates](#-built-in-release-notes--updates)
- [📖 Extension Pages & Navigation](#-extension-pages--navigation)
- [💻 Easy Installation Guide](#-easy-installation-guide)
- [⌨️ Handy Keyboard Shortcuts](#️-handy-keyboard-shortcuts)
- [🔒 Privacy & Data Protection](#-privacy--data-protection)
- [🤝 Feedback & Support](#-feedback--support)
- [📄 License & Disclaimer](#-license--disclaimer)

---

## ✨ Why You'll Love It

Searching for jobs online can quickly become overwhelming. Job feeds are often flooded with third-party staffing agencies, reposted "ghost" jobs, vague qualifications, and roles you've already applied to.

**LinkedIn Job Filter & Analytics Pro** transforms your LinkedIn browsing experience:
- **Save Hours of Scrolling** — Automatically hide listings containing keywords, job titles, or companies you want to avoid.
- **Never Miss Great Opportunities** — Highlight dream roles, remote jobs, and top skill matches with custom glowing badges.
- **See What LinkedIn Hides** — Uncover real applicant numbers, competition tiers, salary details, and actual years of experience required directly on the listing.
- **Stay Organized** — Automatically record when you apply to jobs, track your interview stages, take notes, and export your application history anytime.
- **Total Peace of Mind** — Zero accounts, zero external servers, and zero telemetry. Everything runs entirely on your computer.

---

## 🚀 Key Features

### 🔍 Smart Filtering & Custom Rules
- **One-Click Starter Presets** — Jumpstart your filtering with curated, pre-configured templates:
  - *Hide Staffing Agency Spam* — Automatically filter out recruitment agencies (e.g., CyberCoders, Robert Half, TEKsystems, Apex).
  - *Highlight Remote Roles* — Spot work-from-home and remote opportunities instantly.
  - *Hide Unpaid & Internships* — Clear out unpaid, volunteer, or student internship posts.
  - *Highlight Senior & Leadership Roles* — Prioritize Senior, Staff, Principal, and Lead positions.
  - *Highlight Direct-Hire Positions* — Focus on direct, permanent employment opportunities.
- **Targeted Field Selection** — Choose exactly where to apply your filter rules:
  - **All Fields** — Searches title, company name, and job description snippets.
  - **Job Title Only** — Restricts matching strictly to the job title.
  - **Company Name Only** — Specifically targets or hides specific employers.
- **Negative Keywords (Exclusions / NOT Logic)** — Refine rules to prevent unwanted matches (e.g., match *"Python"* but exclude *"Senior"* or *"Manager"*).
- **Smart Word-Boundary Matching** — Intelligent matching engine avoids false positives (e.g., searching for *"intern"* matches *"Software Intern"*, but never *"International"*).
- **Synonym Suggestions** — Get smart chip suggestions as you type keywords (e.g., typing *"React"* suggests `+ ReactJS`, `+ React.js`; typing *"Node"* suggests `+ NodeJS`).
- **Live Rule Tester** — Test your custom rules against sample job text in real time before saving.
- **Rule Hierarchy & Drag-and-Drop** — Reorder rules easily. Hide rules take precedence over highlights to ensure your feed stays clean.
- **Master Pause Switch** — Temporarily turn off all filtering with a single click from the popup or dashboard whenever you want to see unfiltered results.

---

### 📝 Applied Jobs Tracker
- **Automatic Click Detection** — Automatically detects when you click LinkedIn's "Apply" or "Easy Apply" buttons and records the job in your tracker.
- **"Follow Company" Auto-Unchecker** — Automatically unchecks the "Follow company" box when submitting Easy Apply applications, keeping your LinkedIn feed clean.
- **Undo Countdown Notification** — A friendly floating notification appears when you apply, giving you a chance to cancel or undo before saving.
- **Dedicated Application Dashboard** — Search, filter, and review all your applied jobs in a clean, responsive table.
- **Status Lifecycle Tracking** — Organize your applications across 5 stages: *Applied*, *Reviewing*, *Interviewing*, *Rejected*, and *Offered*.
- **Personal Notes & Contacts** — Add custom notes, interview dates, recruiter names, or salary expectations to any tracked job.
- **Direct Job Links** — Convenient chips let you jump straight back to the original LinkedIn job listing at any time.
- **Date Range Filters & Calendar** — Filter your application history with one click (*Today*, *Yesterday*, *Last 7 Days*, *Last 30 Days*, *This Month*) or pick custom dates.
- **Data Export** — Export your complete job hunting history to **CSV** (for Excel or Google Sheets) or **JSON** with one click.

---

### 📊 Floating Job Insights Widget (HUD)
- **Sleek Floating Overlay** — A modern, compact widget that appears alongside job details to give you immediate insights without getting in your way.
- **Live Applicant Numbers & Competition Gauge** — Shows real-time applicant counts with dynamic competition ratings (*Low*, *Medium*, *High*, *Very High*).
- **Clear Experience Requirements** — Automatically scans job descriptions to extract required and preferred experience levels (e.g., *6 months*, *1–2 years*, *5+ years*).
- **Salary Transparency** — Detects and highlights disclosed compensation ranges (e.g., *$120K – $150K/yr*, *Hourly*).
- **Ghost Job & Stale Listing Warnings** — Identifies listings older than 30 days or repeatedly reposted jobs, helping you avoid wasting time on inactive openings.
- **Workplace Type Badges** — Clearly displays whether a role is *Remote*, *Hybrid*, or *On-site*.
- **Drag & Position Memory** — Drag the widget anywhere on your screen; it remembers your preferred placement across browser sessions.

---

### 📈 Search Analytics & Activity Trends
- **Overview KPI Cards** — See how many listings you've reviewed, hidden, highlighted, and applied to today and throughout your job search.
- **Interactive Visual Charts** — Explore your search and application trends using smooth line graphs, translucent area charts, activity heatmaps, or bubble distribution views.
- **Timeframe Grouping** — View your progress by Day, Week, Month, or Year.
- **Keyword Cloud** — Visual summary showing the skills and keywords that appear most frequently in your matching jobs.
- **One-Click Chart Export** — Download high-resolution PNG images of your charts or export raw data to CSV for your own spreadsheets.

---

### 🎨 Modern Design & Custom Themes
- **4 Tailored Color Themes** — Easily switch between **Light**, **Dark**, **Midnight**, and **Ocean** themes.
- **Instant Theme Switcher** — Toggle themes directly from the toolbar popup with a single click.
- **Live Cross-Tab Sync** — Theme adjustments instantly apply across all open extension pages and tabs without reloading.
- **Clean Typography** — Designed with the modern, legible Inter font for a comfortable reading experience.

---

### ⚙️ Settings, Presets & Data Portability
- **Complete Backup & Restore** — Export all your rules, settings, and application history into a single backup file and restore it whenever you need.
- **Customizable Widget** — Adjust widget visibility and set its default starting position (*Top Right* or *Bottom Right*).
- **Easy Apply Preferences** — Enable or disable the automatic unchecking of the "Follow company" box based on your personal preference.

---

### 📋 Built-In Release Notes & Updates
- **Interactive In-App Changelog** — Browse detailed release notes and feature highlights right inside the extension.
- **Version Filters** — Filter updates by specific versions to see what's new and how the extension has improved.

---

## 📖 Extension Pages & Navigation

Access all tools easily through the extension toolbar popup or the built-in sidebar navigation:

| Page | How to Access | What It's For |
|---|---|---|
| **Toolbar Popup** | Click extension icon in Chrome | Quick master switch, today's stats, theme toggle, and 1-click link to LinkedIn Jobs |
| **Rules Dashboard** | Sidebar → Dashboard (`Alt+Shift+D`) | View, create, edit, search, and organize your filtering and highlight rules |
| **Applied Jobs** | Sidebar → Applied Jobs | Manage submitted applications, update interview statuses, add notes, and export |
| **Statistics** | Sidebar → Statistics | Interactive charts, job hunt activity trends, and keyword frequency cloud |
| **Settings** | Sidebar → Settings | Change themes, configure the floating widget, and backup or restore your data |
| **Changelog** | Sidebar → Changelog | Browse the latest updates, enhancements, and feature release notes |
| **About Maker** | Sidebar → About Maker | Project background, creator showcase, storage health diagnostics, and support |
| **Rule Editor** | Dashboard → New Rule / Edit | Set up custom keywords, fields, exclusions, and test matching in real time |

---

## 💻 Easy Installation Guide

Getting started takes less than a minute. No coding, command line, or technical tools required:

1. **Download the Extension**
   - Click the green **Code** button at the top of the repository page and select **Download ZIP**.
   - Save the file to your computer and extract (unzip) the folder.

2. **Open Chrome Extensions**
   - In Google Chrome, type `chrome://extensions` in the address bar and press **Enter**.
   - (Alternatively, click the three vertical dots menu in Chrome → **Extensions** → **Manage Extensions**).

3. **Turn on Developer Mode**
   - In the top-right corner of the Extensions page, switch the **Developer mode** toggle to **ON**.

4. **Load the Extension**
   - Click the **Load unpacked** button in the top-left corner.
   - Select the unzipped `LinkedIn-Job-Filter-Analytics-Pro` folder.

5. **Pin the Extension**
   - Click the puzzle piece icon (Extensions) in your Chrome toolbar next to your profile picture.
   - Click the pin icon next to **LinkedIn Job Filter & Analytics Pro** so it's always accessible.

6. **Start Browsing!**
   - Go to [LinkedIn Jobs](https://www.linkedin.com/jobs/) and your filter rules and floating widget will be active automatically.

---

## ⌨️ Handy Keyboard Shortcuts

Boost your efficiency while managing your job search:

| Shortcut | Where It Works | What It Does |
|---|---|---|
| `Alt+Shift+D` | Anywhere in Chrome | Instantly opens the Rules Dashboard |
| `Escape` | Modals & Dialogs | Closes any open modal, rule editor, or popup window |
| `Enter` | Rule Editor | Commits and adds a keyword or exclusion chip |

---

## 🔒 Privacy & Data Protection

Your job search is personal, and your privacy is our top priority:

- **100% On-Device Processing** — All your custom rules, notes, applied jobs history, and statistics are stored locally on your machine via Chrome's storage system.
- **Zero External Telemetry** — Nothing you search, view, or apply for is ever transmitted to an external server or third party.
- **No Account Required** — No signups, logins, or tracking pixels. The extension is completely ready to use the moment it's installed.
- **Transparent & Open Source** — The full source code is completely open, auditable, and accessible to anyone.

---

## 🤝 Feedback & Support

- **Found a bug or have a suggestion?** Open an issue on this repository to share your thoughts.
- **Love using the extension?** Give this repository a ⭐ star to help other job seekers discover it!
- **Support Continued Development**: If this tool has saved you time in your job search, consider [buying the creator a coffee](https://buymeacoffee.com/thecaptaincook).

---

## 📄 License & Disclaimer

This project is open-source and released under the **MIT License with Attribution & Indemnification Shield** — see the [`LICENSE`](../LICENSE) file for complete terms.

### Key Points:
- **Author Attribution**: Free to use, modify, and distribute provided that original credit to creator Masem ([@TheCaptainCook](https://github.com/TheCaptainCook)) is prominently preserved.
- **Disclaimer**: This software is provided "as is", without warranty of any kind.
- **Non-Affiliation**: This extension is an independent open-source project and is not affiliated with, endorsed by, sponsored by, or associated with LinkedIn Corporation or Microsoft Corporation.
