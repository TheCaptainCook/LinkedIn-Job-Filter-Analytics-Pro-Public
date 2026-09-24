<p align="center">
  <img src="assets/banner.png" alt="LinkedIn Job Filter & Analytics Pro Banner" width="100%">
</p>

# LinkedIn Job Filter & Analytics Pro

<p align="center">
  <a href="https://developer.chrome.com/docs/extensions/mv3/intro/"><img src="https://img.shields.io/badge/Manifest-V3-orange.svg?style=flat-square" alt="Manifest Version"></a>
  <a href="https://chrome.google.com/webstore"><img src="https://img.shields.io/badge/Chrome-Extension-4285F4.svg?style=flat-square&logo=google-chrome&logoColor=white" alt="Chrome Extension"></a>
  <img src="https://img.shields.io/badge/version-1.2.6-blue.svg?style=flat-square" alt="Version 1.2.6">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT%20%2B%20Indemnification-blue.svg?style=flat-square" alt="License: MIT with Indemnification Shield"></a>
  <img src="https://img.shields.io/badge/Pure-JavaScript%20(No%20Dependencies)-blueviolet.svg?style=flat-square" alt="Zero Dependencies">
  <img src="https://img.shields.io/badge/Privacy-100%25%20Local%20Processing-brightgreen.svg?style=flat-square" alt="100% Local">
</p>

A modern, professional-grade Chrome Extension that declutters and supercharges your LinkedIn job search. Create custom keyword rules to auto-hide irrelevant listings, highlight high-priority opportunities, surface hidden job metadata (applicants, salary, required experience, ghost job flags) with a sleek floating HUD stats widget, and track search metrics over time — all processed **100% locally** in your browser with zero external telemetry.

---

## 📑 Table of Contents

- [🚀 Key Features](#-key-features)
  - [🔍 Smart Filtering & Rule Management](#-smart-filtering--rule-management)
  - [📝 Applied Jobs Tracker](#-applied-jobs-tracker)
  - [📊 Floating Job Stats Widget](#-floating-job-stats-widget)
  - [📋 Interactive Changelog & Release Notes](#-interactive-changelog--release-notes)
  - [🎨 Modern Design System & Themes](#-modern-design-system--themes)
  - [📈 Statistics & Analytics](#-statistics--analytics)
  - [⚙️ Settings, Presets & Data Portability](#️-settings-presets--data-portability)
- [🛡️ Security Hardening & Architecture](#️-security-hardening--architecture)
- [🛠 Installation (Developer / Unpacked)](#-installation-developer--unpacked)
- [📖 Navigation & Pages](#-navigation--pages)
- [🏗 Repository Architecture](#-repository-architecture)
- [⌨️ Keyboard Shortcuts](#️-keyboard-shortcuts)
- [📋 Changelog](#-changelog)
- [🔒 Privacy & Data Protection](#-privacy--data-protection)
- [🤝 Contributing](#-contributing)
- [📄 License & Disclaimer](#-license--disclaimer)

---

## 🚀 Key Features

### 🔍 Smart Filtering & Rule Management
- **Curated Starter Presets** — 1-click templates ready to import:
  - *Hide Agency / Staffing Spam* (e.g., CyberCoders, Robert Half, TEKsystems, Apex)
  - *Highlight Remote Opportunities* (e.g., Remote, Work from Anywhere)
  - *Hide Unpaid / Internships* (e.g., Unpaid, Volunteer, Student Intern)
  - *Highlight Senior / Staff Roles* (e.g., Senior, Staff, Principal, Lead)
  - *Highlight Direct Hire Opportunities* (Direct Hire, Full-Time Permanent)
- **Target Field Selection** — Target keyword rules specifically to:
  - **All Fields** (searches Title, Company Name, and Full Card Snippet)
  - **Job Title Only** (strict title match)
  - **Company Name Only** (target or hide specific employers)
- **Negative Keywords (Exclusions / NOT Logic)** — Exclude specific words from triggering a rule (e.g., target *"Python"* but exclude *"Senior"* or *"Manager"*).
- **Boundary-Aware Keyword Matching** — Smart word-boundary regex engine prevents false positives (e.g., searching *"intern"* matches *"Software Intern"*, but never *"International"*).
- **Smart Synonym Suggestions** — Dynamic chip suggestions when authoring rules (e.g., typing *"React"* suggests `+ ReactJS`, `+ React.js`; typing *"Node"* suggests `+ NodeJS`).
- **Interactive Live Rule Tester** — Test rules against sample job text directly inside the Rule Editor with instant match feedback.
- **Priority Precedence** — Drag-and-drop or reorder rules to establish execution hierarchy (Hide rules override Highlights; top Highlight determines card styling and badge).
- **Dedicated Dashboard Action Bar** — Ergonomic split layout grouping Rule Creation and Starter Presets on the left, with the master filtering switch and live status beacon anchored on the right.
- **Master Pause Switch** — Instantly pause or resume all filtering on the fly from the toolbar popup or dashboard header.

### 📝 Applied Jobs Tracker
- **Automated Click Detection** — Detects clicks on LinkedIn's "Apply" and "Easy Apply" buttons across detail panes and search feed cards.
- **Interactive Application Link Chips** — Dynamic clickable chips in the Apply Type column for fast access:
  - **Easy Apply Chip**: Opens the LinkedIn job listing in a new tab (`⚡ Easy Apply`).
  - **LinkedIn Chip**: Standard direct link to the LinkedIn job post for standard applications (`LinkedIn`).
- **Equal-Width Table Layout & Centered Column Geometry** — Consolidated all URL actions directly into the Apply Type chip strip with strictly equal column widths (14.285% each on desktop) and centered cell alignment, providing a clean, horizontal-scroll-free layout.
- **Easy Apply "Follow Company" Auto-Unchecker** — Automatically unchecks the "Follow company" checkbox on Easy Apply modal submissions, with full manual override detection and configurable toggle in Settings.
- **Undoable Countdown Timer** — Floating, non-intrusive status notification with an animated countdown timer giving you time to cancel or undo before auto-recording.
- **Dedicated Management Dashboard (`pages/applied.html`)** — Filter, search, and manage your job applications in a responsive tabular view.
- **Status Lifecycle Tracking** — Update application progress across 5 stages (*Applied*, *Reviewing*, *Interviewing*, *Rejected*, *Offered*) with custom notes.
- **Manual Job Entry & Edit Modal** — Add or update jobs applied to on or outside LinkedIn with unified fields for URLs, notes, and statuses.
- **Data Portability & Export** — One-click export of complete application logs to CSV (with clean Job URL column) and JSON formats.

### 📊 Floating Job Stats Widget
- **Sleek HUD Silhouette** — Compact 210px width with an elegant vertical aspect ratio, generous row spacing, and deep glassmorphic styling across all themes.
- **Live Applicant Count & Competition Badges** — Real-time applicant extraction with dynamic competition intensity badges (*Low*, *Medium*, *High*, *Very High*).
- **Transparent Experience Parsing** — Multi-tier regex engine parses minimum and preferred experience requirements directly from job descriptions, supporting both year and month-based criteria (`6 months`, `1-2 years`, `3+ years`), word numbers (1–20), and section-aware qualification detection (`Preferred Qualifications`, `Minimum / Basic Qualifications`, `Requirements`).
- **High-Volume Applicant Transparency Tooltip** — For listings with 100+ applications (where selection odds are statistically near-impossible), deep parsing is gracefully bypassed for browsing speed. An interactive circular `(i)` info icon provides an appealing popover explaining this logic.
- **Salary Transparency Scraper** — Automatically detects and normalizes disclosed compensation ranges (e.g., *$120K – $150K/yr*, *£60K – £80K*, *Hourly*).
- **Ghost Job & Stale Listing Detection** — Identifies closed/reposted listings and old posts (>30 days) taking applications, highlighting them with warning badges.
- **Structured Location & Time Rows** — Dedicated rows for location (with Remote, Hybrid, and On-site badges) and posted date.
- **Two-Line Job Titles** — Graceful multiline title rendering that prevents abrupt truncations.
- **Intelligent DOM-Settle Scheduler** — Eliminates race conditions during page loads, browser history navigation, and pagination, ensuring the widget never freezes or stamps empty placeholder cards.
- **Proportional Drag Memory** — Drag anywhere on the header; widget remembers its exact relative viewport position across window resizing.

### 📋 Interactive Changelog & Release Notes
- **In-Extension Release Notes (`pages/changelog.html`)** — Dedicated interactive release viewer built directly into the extension dashboard.
- **Timeline & Version Filter Chips** — Filter updates by specific version (`v1.2.6`, `v1.2.5`, `v1.2.4`, etc.) or browse the complete chronological release history.
- **Streamlined Timeline View** — Dedicated vertical version timeline with generous visual spacing, glowing status milestones, and responsive layout.
- **Summary Metrics** — High-level KPI summary of total releases, active major features, and continuous performance updates.

### 👨‍💻 Maker & Architectural Mission
- **Creator Showcase (`pages/about.html`)** — Dedicated About the Maker page spotlighting creator Masem ([@TheCaptainCook](https://github.com/TheCaptainCook)).
- **Core Engineering Pillars** — Explores 100% Client-Side Privacy, Zero-Latency Performance, Candidate Transparency, and Open-Source Community.
- **Diagnostics & Storage Health** — Live inspection tiles displaying active filter rule counts, tracked applications count, and storage consumption directly from Chrome Storage API.
- **One-Click Repository Actions** — Interactive copyable Git clone command with instant toast feedback and direct repository navigation.
- **Support the Maker** — [Buy Me a Coffee](https://buymeacoffee.com/thecaptaincook) to fuel continuous open-source feature development and maintenance.

### 🎨 Modern Design System & Themes
- **Typography** — Clean, legible **Inter** font applied seamlessly across the Dashboard, Statistics, Settings, Rule Editor, Popup, and in-page widgets.
- **Consistent Header Shell** — Uniform headers, title typography, and quick LinkedIn launchers across Dashboard, Applied, Stats, Settings, and Changelog.
- **Cohesive Interactive Components** — Buttons with smooth gradients, subtle depth, micro-interactions, and glowing hover states.
- **Quick-Access Job Search** — Direct one-click fancy button in the toolbar popup linking straight to `linkedin.com/jobs/search/`.
- **4 Tailored Themes** — Instant switching between **Light**, **Dark**, **Midnight**, and **Ocean** color palettes with zero flicker (FOWT prevention via render-blocking theme loader).
- **Live Cross-Tab Theme Sync** — Theme adjustments made on any page propagate live across all open extension tabs and windows instantly without manual reloading.

### 📈 Statistics & Analytics
- **KPI Summary Cards** — Track total listings reviewed, hidden, and highlighted today and all-time, alongside applications submitted.
- **Dual Multi-Chart Visualization Engines** — Full feature parity across both **Activity Trends** and **Applied Jobs Trends**, each offering 4 interactive chart modes (*Smooth Line Graph*, *Translucent Area Chart*, *Activity Heatmap*, *Bubble Distribution*) with Day, Week, Month, and Year intervals.
- **Enhanced Visual Splines** — Smooth cubic Bézier interpolation curves with glowing halo dots replacing rigid polyline segments.
- **Streamlined Trend Controls** — Pure focus on applications count, date range intervals, and instant export options.
- **High-Resolution Exports** — One-click PNG image export for presentation slides and full CSV spreadsheet downloads for custom data analysis.
- **Keyword Cloud** — Visual frequency map of your most frequently matched keywords, color-coded by action.
- **Screen Reader Accessible** — Dynamic text summaries and ARIA labels for all canvas chart visualizations.

### ⚙️ Settings, Presets & Data Portability
- **Complete JSON Backup & Restore** — Export and import all rules and analytics data with built-in schema validation, 2MB payload guard, and 500-rule limit protections.
- **Self-Updating Schema Migrations** — Automatically upgrades rule formats across extension versions without data loss.
- **Widget Customization** — Toggle widget visibility and configure default anchor points (*Top Right* / *Bottom Right*).

---

## 🛡️ Security Hardening & Architecture

The extension codebase has undergone comprehensive security hardening and optimization:

- **DOM-Based XSS Prevention** — All dynamic UI injections (toasts, confirmation dialogs, modal popups, tooltip overlays, rule lists) utilize strict HTML entity escaping (`escapeHtml()`) and safe DOM text/attribute assignment instead of vulnerable string concatenations.
- **Prototype Pollution Defense** — Object cloning and state migration mechanisms feature explicit key sanitization that unconditionally strips `__proto__`, `constructor`, and `prototype` keys before processing.
- **Strict Import Boundary Validation** — JSON backup imports enforce strict schema checks, a 2MB maximum payload size limit, property type enforcement, and record capping (max 500 rules) to prevent memory exhaustion and DoS vectors.
- **Main-World Defensive Interception** — The native page-world script ([`injected.js`](scripts/injected.js)) utilizes private `Symbol` guards to prevent double-wrapping, bounded LRU caches (50 items) for network payload deduplication, and isolated `try/catch` boundaries to guarantee zero interference with LinkedIn's application code.
- **Strict Content Security Policy (CSP)** — Zero inline scripts (`script-src 'self'`) and zero inline event handlers across all extension HTML views (`popup.html`, `options.html`, `stats.html`, `settings.html`, `condition.html`, `applied.html`, `changelog.html`).
- **Resource Protocol Whitelisting** — Strict protocol and domain validation (`https://` against verified LinkedIn CDN origins) for all rendered company logos.
- **Dual-Mode Settle Scheduler** — Combined fast rAF observer for normal browsing with an adaptive 350ms settle debounce for complex single-page-app navigation and pagination transitions, preventing race conditions.
- **Accessibility & Focus Trapping** — WAI-ARIA compliant modal dialogs featuring `role="dialog"`, `aria-modal="true"`, focus cycle trapping, and keyboard `Escape` dismissal handlers.
- **Modern ES6+ Standards** — Complete transition to block-scoped `const`/`let` bindings across all content scripts and background services.
- **Structured Diagnostic Logging** — Replaced silent failures with centralized `[HAJL]` prefixed error logging for rapid diagnosis and transparent debugging.

---

## 🛠 Installation (Developer / Unpacked)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/TheCaptainCook/LinkedIn-Job-Filter-Analytics-Pro-Public.git
   ```
2. Open Google Chrome and navigate to `chrome://extensions/`
3. Enable **Developer mode** (toggle in the top-right corner)
4. Click **Load unpacked** and select the cloned `LinkedIn-Job-Filter-Analytics-Pro-Public` folder
5. Pin the extension icon to your Chrome toolbar for quick access

---

## 📖 Navigation & Pages

| Page | Access Point | Purpose |
|---|---|---|
| **Toolbar Popup** | Extension Icon in Browser | Master pause toggle, session stats, quick link to LinkedIn Jobs |
| **Dashboard** | Sidebar → Dashboard (`Alt+Shift+D`) | Manage, reorder, search, filter, and batch-edit rules; access Starter Presets |
| **Applied Jobs** | Sidebar → Applied Jobs | Track and manage applied job listings, status lifecycles, notes, and CSV/JSON exports |
| **Statistics** | Sidebar → Statistics | Interactive charts, summary tiles, keyword frequency cloud, PNG/CSV exports |
| **Settings** | Sidebar → Settings | Theme selection, stats widget options, complete JSON backup & restore |
| **Changelog** | Sidebar → Changelog | Interactive version timeline, version filter chips, search, and release notes |
| **About Maker** | Sidebar → About Maker | Creator showcase, engineering pillars, live storage diagnostics, Buy Me a Coffee support |
| **Rule Editor** | Dashboard → New Rule / Edit | Configure target fields, keywords, synonyms, exclusions, and live test matches |

---

## 🏗 Repository Architecture

The codebase is organized into clean, modular subdirectories grouping related logic:

```
LinkedIn-Job-Filter-Analytics-Pro/
├── manifest.json               ← MV3 extension manifest (permissions, content scripts, shortcuts)
├── assets/                     ← Extension icons, banner, and graphic assets
│   ├── banner.png
│   ├── icon16.png
│   ├── icon48.png
│   └── icon128.png
├── docs/                       ← Architecture guides, reviews, and contributing docs
│   ├── ARCHITECTURE.md         ← Technical architecture, storage layout & schema design
│   ├── CHANGELOG.md            ← Standard user-facing release notes and version history
│   ├── CHANGELOG-TECHNICAL-DETAILS.md ← Comprehensive developer technical changelog
│   ├── CONTRIBUTING.md         ← Contribution guidelines and code style rules
│   └── codebase_review.md      ← Code quality and security review documentation
├── pages/                      ← Extension HTML views (served in tabs & popup)
│   ├── popup.html              ← Toolbar popup with quick LinkedIn search button & session stats
│   ├── options.html            ← Rules Dashboard (search, filters, bulk ops, presets modal)
│   ├── applied.html            ← Applied Jobs tracking dashboard (table, search, filters, modal)
│   ├── stats.html              ← Analytics dashboard with Canvas charts & CSV/PNG export
│   ├── settings.html           ← Settings panel (theme, widget config, data backup/restore)
│   ├── condition.html          ← Rule editor with field targeting, exclusions, synonyms & tester
│   └── changelog.html          ← Changelog dashboard (version timeline, filter chips & search)
├── scripts/
│   ├── background.js           ← Service worker (metrics, badge updater, shortcuts, auto-migration)
│   ├── injected.js             ← Main-world script (intercepts LinkedIn Voyager API responses)
│   ├── shared/                 ← Cross-context shared utilities & components
│   │   ├── utils.js            ← Centralized utility helpers (escaping, dates, safe parsing, [HAJL] logging)
│   │   ├── theme.js            ← Render-blocking theme loader & cross-tab theme sync
│   │   └── sidebar.js          ← Shared navigation sidebar injector
│   ├── pages/                  ← Dedicated controllers for extension HTML views
│   │   ├── options.js          ← Rules dashboard logic (presets, search, filters, bulk actions)
│   │   ├── applied.js          ← Applied Jobs tracker logic (CRUD, filters, status lifecycle, export)
│   │   ├── popup.js            ← Extension toolbar popup logic & master switch
│   │   ├── settings.js         ← Settings page logic (themes, widget preferences, backup/restore)
│   │   ├── stats.js            ← Statistics page logic & export handlers
│   │   ├── condition.js        ← Rule editor form, synonym suggestions & live regex tester
│   │   └── changelog.js        ← Changelog controller (version chip filters & live search)
│   ├── charts/                 ← Canvas chart rendering engine
│   │   ├── chart.js            ← Chart aggregation orchestrator & tooltip handler
│   │   ├── lineGraph.js        ← Smooth Bézier line graph renderer
│   │   ├── areaChart.js        ← Smooth Bézier translucent area chart renderer
│   │   ├── heatmap.js          ← Activity heatmap renderer
│   │   ├── bubbleChart.js      ← Bubble distribution chart renderer
│   │   └── appliedChart.js     ← Applied jobs multi-chart engine (Line, Area, Heatmap, Bubble)
│   └── content/                ← Content scripts injected into LinkedIn
│       ├── main.js             ← MutationObserver orchestrator & navigation handler
│       ├── jobs.js             ← Card fingerprinting, field targeting & rule evaluation
│       ├── applyTracker.js     ← Auto-tracking for Apply / Easy Apply button clicks
│       ├── scraper.js          ← Main scraper orchestrator
│       ├── ui.js               ← Stats widget overlay, stale badges, salary row & highlight styles
│       ├── settings.js         ← Settings cache & storage synchronization
│       ├── statsTracker.js     ← Telemetry batching & badge count sync
│       └── scraper/            ← Modular scraping sub-engines
│           ├── applicants.js   ← Live applicant count extraction
│           ├── domScraper.js   ← Card DOM parsing & fallback extraction
│           ├── experience.js   ← Multi-tier regex experience parser (months & years)
│           ├── identity.js     ← Company name & logo extraction
│           └── salary.js       ← Compensation range parser & normalizer
└── styles/
    ├── layout.css              ← App shell layout, sidebar styling, and fancy buttons
    └── content/
        ├── highlight.css       ← Job card highlighting, session unhide, and hide animations
        └── stats.css           ← Sleek floating stats widget HUD styling & themes
```

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Scope | Action |
|---|---|---|
| `Alt+Shift+D` | Global (Browser) | Open the Rules Dashboard |
| `Escape` | Modals & Dialogs | Close active modal or dialog |
| `Tab` / `Shift+Tab` | Modals | Trap and cycle keyboard focus inside modal |
| `Enter` | Rule Editor Chips | Commit keyword or exclusion tag |

---

## 📋 Changelog

- **User-Facing Release Notes**: See [`docs/CHANGELOG.md`](docs/CHANGELOG.md) or open the interactive in-extension viewer (`pages/changelog.html`).
- **Developer Technical Details**: See [`docs/CHANGELOG-TECHNICAL-DETAILS.md`](docs/CHANGELOG-TECHNICAL-DETAILS.md) for full module paths, DOM selectors, regex patterns, and implementation notes.

## 🔒 Privacy & Data Protection

- **100% Local Processing** — All rules, filter criteria, scraped metadata, and statistics remain stored locally in your browser via `chrome.storage.local` and `chrome.storage.sync`.
- **Zero External Telemetry** — No search queries, user data, credentials, or browsing history are ever transmitted to any third-party server.
- **Message Verification** — Internal Chrome extension messaging strictly verifies sender integrity (`sender.id === chrome.runtime.id`).
- **Defensive Main-World Boundary** — Page-world hooks do not expose extension internals and operate within isolated execution contexts.
- **Open Source & Transparent** — Full source code is open and audit-ready under the MIT License with Attribution & Indemnification Shield.

---

## 🤝 Contributing

Contributions are welcome! Please read our [`CONTRIBUTING.md`](docs/CONTRIBUTING.md) and [`ARCHITECTURE.md`](docs/ARCHITECTURE.md) to get started.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'feat: add AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License & Disclaimer

This project is licensed under the **MIT License with Attribution & Indemnification Shield** — see the [`LICENSE`](LICENSE) file for the complete legal text.

### Key Terms & Protections:
- **Mandatory Author Attribution**: You are permitted to use, copy, modify, merge, publish, and distribute this software, provided that **explicit credit to the original author (Masem / [@TheCaptainCook](https://github.com/TheCaptainCook))** and the repository link are prominently retained in all copies, forks, substantial portions, derivative works, and user-facing documentation.
- **Strict Limitation of Liability**: The software is provided "AS IS", without warranty of any kind. Under no legal theory (contract, tort, negligence, or otherwise) shall the author or copyright holders be liable for any direct, indirect, incidental, consequential, or punitive damages, account restrictions/terminations, or third-party disputes.
- **Comprehensive User Indemnification Shield**: Any user, developer, or distributor agrees to defend, indemnify, and hold entirely harmless the author and copyright holder from and against any claims, demands, lawsuits, proceedings, liabilities, damages, fines, or legal expenses (including reasonable attorney fees) arising from their access, use, modification, distribution, or any violation of third-party terms of service (such as LinkedIn Corporation's User Agreement or automation policies).
- **Non-Affiliation**: This extension is an independent open-source project and is not affiliated with, authorized by, sponsored by, or endorsed by LinkedIn Corporation or Microsoft Corporation.

