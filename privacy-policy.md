# Privacy Policy for LinkedIn Job Filter & Analytics Pro

**Effective Date:** September 27, 2026  
**Last Updated:** September 27, 2026  
**Developer / Maintainer:** Masem ([@TheCaptainCook](https://github.com/TheCaptainCook))  
**Repository:** ([https://github.com/TheCaptainCook/LinkedIn-Job-Filter-Analytics-Pro](https://github.com/TheCaptainCook/LinkedIn-Job-Filter-Analytics-Pro-Public))

---

## 1. Introduction & Core Philosophy

**LinkedIn Job Filter & Analytics Pro** ("the Extension", "we", "our") is an open-source, client-side productivity extension designed to help job seekers filter, analyze, and track employment opportunities on LinkedIn.

We believe that job search data is deeply personal. Your career ambitions, application history, target companies, interview notes, and keyword preferences belong solely to you.

**Our Core Privacy Guarantee:**
* **100% Local Processing**: All keyword filtering, metadata extraction, application tracking, and analytics aggregation occur strictly inside your local browser runtime.
* **Zero External Telemetry**: The extension operates with zero remote servers. We do not operate an API server, database, or analytics backend.
* **Zero Tracking or Selling**: We never collect, transmit, monetize, track, or sell your personal information, search queries, browsing habits, or LinkedIn activity.

---

## 2. What Information We Handle (And How It Is Stored)

The Extension handles only the data required to deliver its core job search and filtering capabilities. All data is stored within your browser's private extension storage sandbox:

### A. Custom Filtering Rules & Preferences
* **Data Handled**: Custom keywords, exclusion terms (NOT logic), rule names, target fields (All Fields, Job Title, Company), match actions (Hide or Highlight), and chosen accent colors.
* **Storage Location**: `chrome.storage.sync` (and `chrome.storage.local` fallback).
* **Purpose**: To evaluate job listings on LinkedIn against your preferences and sync your rules across your personal Chrome profiles.

### B. Applied Jobs Tracker Log
* **Data Handled**: Company name, job title, LinkedIn Job ID, application URL, applicant count at time of application, required experience string, applied timestamp, application method ("Easy Apply" or "External Apply"), status lifecycle stage (Applied, Reviewing, Interviewing, Rejected, Offered), and optional personal notes authored by you.
* **Storage Location**: `chrome.storage.local`.
* **Purpose**: To display your application history on the Applied Jobs dashboard, populate the row-inspection details modal, enable multi-date range filtering, and allow you to auto-hide postings you have already applied to.

### C. Extension Settings & UI Configuration
* **Data Handled**: Floating stats HUD toggle and screen position (Top-Right or Bottom-Right), Easy Apply automation preferences (auto-uncheck follow company, auto-click "Not now" on post-application popups), Dynamic URL filter persistence toggle, and visual theme selection (Light, Dark, Midnight, Ocean).
* **Storage Location**: `chrome.storage.sync` and `chrome.storage.local`.
* **Purpose**: To preserve your interface preferences across browser sessions.

### D. Keyword Aggregation Metrics
* **Data Handled**: Daily and hourly aggregate counters of hidden vs. highlighted job postings, and top triggered keyword counts.
* **Storage Location**: `chrome.storage.local`.
* **Purpose**: To render your local keyword intelligence charts and filtering volume trends on the Analytics page.

---

## 3. What Information We NEVER Collect

The Extension does **NOT** collect, access, log, or transmit:
* **No Account Credentials**: We never access, capture, or store your LinkedIn username, password, two-factor authentication tokens, or session cookies.
* **No Personal Identity Information (PII)**: We do not collect your real name, email address, telephone number, mailing address, resume/CV files, or profile photos.
* **No Private Communications**: We do not access or read your LinkedIn InMail messages, direct chats, network invitations, or connection lists.
* **No Cross-Site Browsing History**: The extension does not inspect, monitor, or record your browsing activity on any website outside `https://www.linkedin.com/jobs/*`.
* **No Third-Party Analytics**: We do not embed Google Analytics, Mixpanel, Segment, Sentry, Facebook Pixels, or any third-party tracking libraries.

---

## 4. Permissions & Justification

The Extension requests only the minimum permissions necessary to function, strictly adhering to Google's Principle of Least Privilege:

| Permission | Purpose & Scope |
|---|---|
| `storage` | Stores your custom filter rules, application logs, and settings locally in your browser. |
| `unlimitedStorage` | Prevents data loss when you accumulate extensive job application logs and notes over multi-month career searches. |
| `activeTab` | Temporarily reads the active LinkedIn search tab URL when you explicitly click "Apply Filters" in the popup to merge selected filter parameters. |
| `https://www.linkedin.com/*` | Injects content scripts strictly into LinkedIn to parse job cards, display the floating HUD widget, and detect application button clicks. |

No access is requested or permitted for any other domain or protocol on the internet.

---

## 5. Third-Party Disclosures & Data Sharing

Because the Extension operates 100% client-side with no remote server infrastructure:
* We **do not share, sell, rent, or trade** your information with any third party.
* We **do not transfer** user data to data brokers, ad networks, or commercial analytics firms.
* We **do not use** user data for credit scoring, personalized advertising, or automated profiling.

---

## 6. User Data Control, Export & Deletion Rights

You have absolute sovereignty over your data at all times:

* **Export Your Data**: You can download a complete backup of all rules, settings, analytics, and tracked applications in standard JSON or CSV formats at any time from the Settings and Applied Jobs pages.
* **Delete Specific Data**: You can edit or delete individual rules, application entries, and notes at any time from their respective dashboards.
* **Reset Analytics**: You can clear all daily and keyword analytics history with one click from the Settings page.
* **Factory Reset All Data**: You can permanently wipe all stored extension data (rules, logs, metrics, preferences) using the "Reset to Defaults" button in Settings.
* **Complete Uninstallation**: Removing the Extension from Chrome instantly and permanently deletes all data stored in `chrome.storage.local` and `chrome.storage.sync` by your browser.

---

## 7. Children's Privacy

The Extension is designed for working professionals and job seekers. We do not knowingly collect or maintain information from individuals under the age of 13 (or under the applicable age of digital consent in your jurisdiction).

---

## 8. Compliance with Global Privacy Frameworks

* **GDPR (General Data Protection Regulation)**: The Extension processes data under the principle of data minimization and storage limitation. Processing occurs exclusively on the data subject's terminal equipment.
* **CCPA / CPRA (California Consumer Privacy Act)**: We do not "sell" or "share" personal information as defined by California privacy statutes.
* **Google Chrome Web Store Developer Program Policies**: The Extension fully complies with the Chrome Web Store User Data Policy, Single Purpose Policy, and Limited Use requirements.

---

## 9. Changes to This Privacy Policy

If we modify this Privacy Policy, we will update the "Last Updated" date at the top of this document and publish the revised policy in our public GitHub repository and Chrome Web Store listing. Because we collect no contact information, we encourage users to review the repository release notes for updates.

---

## 10. Contact & Open Source Verification

Because LinkedIn Job Filter & Analytics Pro is open-source software, you can independently inspect and verify every line of code to confirm our privacy protections:

* **GitHub Repository**: ([https://github.com/TheCaptainCook/LinkedIn-Job-Filter-Analytics-Pro](https://github.com/TheCaptainCook/LinkedIn-Job-Filter-Analytics-Pro-Public))
* **Author Contact**: Masem ([@TheCaptainCook](https://github.com/TheCaptainCook))
