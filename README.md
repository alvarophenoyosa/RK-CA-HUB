# RK | CA - HUB

A responsive personal study dashboard for CA-PRC preparation. The app is currently a **single-file HTML MVP** with embedded CSS and JavaScript, so it has no build step or package installation.

## Publish with GitHub Pages
1. Open this repository's **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **GitHub Actions**.
3. Open the **Actions** tab and check the **Deploy to GitHub Pages** workflow. The workflow runs on pushes to `main`, and can also be started manually.
4. Once the workflow succeeds, open the published URL shown under **Settings → Pages** or in the workflow deployment summary.

## Run locally
Download `index.html` and open it in a modern browser. For best behaviour with local PDF storage, use a small local web server (for example, VS Code Live Server) rather than a browser's private mode.

## Current features
- Home dashboard with mock history, topic coverage, study-session time, and revision reminders.
- Mock simulator with timer, chapter filter, question navigation, score report, and a local mistakes bank.
- JSON question-bank import. Allowed subject IDs: `prc1-fa`, `prc2-qm`, `prc2-fm`, `prc3-bi`, `prc3-eco`.
- Personal topic tracker, simple mind-map view, formula references, interest/annuity calculators, and an illustrative linear demand/supply graph.
- Student profile, progress snapshot, export/import of study data, and a live personal performance report.
- Personal PDF files are stored in the current browser using IndexedDB; they are not sent to GitHub.

## Important limitations
- The small built-in MCQ pool is explicitly labelled **illustrative demo content**, not official ICAP question-bank content. Import source-backed questions before relying on mocks as exam practice.
- Progress, profile, mock history, and mistakes are stored locally in the browser. They do not sync across devices or between users. Export a backup periodically.
- The generated “Merit” report is a personal study report, not an official ICAP merit list or exam result.
- This is a frontend prototype, not a multi-user app. Authentication, cloud sync, server-side storage, and cross-device persistence are not implemented.

## PDF and study resources
Upload only material you are authorised to use. PDFs uploaded into the app are saved in the user's browser storage, not committed to this repository.
