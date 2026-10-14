# RK | CA - HUB

A responsive CA-PRC personal study dashboard with a neon cyber interface, selectable themes, mock exams, subject progress, study utilities, and a local PDF vault. It is a **single-file HTML MVP** with no package install or build step.

## Themes
- **Neon Grid** — original dark cyber grid.
- **Jet Black Neon** — near-black canvas with cyan/magenta neon.
- **Clean White** — light, clean study workspace.
- **Old-School Classic** — paper-and-ledger inspired cream/forest palette.

Theme choice is saved in browser-local settings. Mock scores are colour-scaled from red through amber to green; subject coverage bars use separate subject colours.

## Publish with GitHub Pages
1. Open repository **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **GitHub Actions**.
3. Open the **Actions** tab and check **Deploy to GitHub Pages**. The workflow runs on pushes to `main` and can also be started manually.
4. Once successful, open the published URL shown under **Settings → Pages** or in the workflow deployment summary.

The workflow cannot enable Pages if GitHub's repository settings or app permissions prohibit creating the Pages site; in that case enable Pages manually in Settings → Pages and rerun the workflow.

## Run locally
Download `index.html` and open it in a modern browser. For more reliable local PDF storage, use a local web server (for example, VS Code Live Server) and avoid private browsing mode.

## Current features
- HOME: study-time and streak metrics, subject coverage, recent mock attempts, and revision reminders.
- MOCK: timed one-question-at-a-time MCQ simulator, question navigation, score report, mistakes bank, and JSON question-bank import.
- STUDY: local PDF vault, course PDF catalogue, topic tracker, mind-map workspace, formula references, interest/annuity calculators, and an illustrative Economics demand/supply plotter.
- PROFILE: student details, target date, topic coverage, study time, mock average, weak/strong subjects, and data export/import.
- MERIT: personal live progress report, subject performance table, and export.
- Four themes and score-dependent red → amber → green colours.

## PRC course PDF catalogue status
The app lists the eight PDF files previously uploaded to the project workspace:
- PRC 1 Financial Accounting Study Text and Question Bank
- PRC 2 Volume 1 Quantitative Methods Study Text and Question Bank
- PRC 3 Volume 1 Business Insights Study Text and MCQs
- PRC 3 Volume 2 Economics Study Text and MCQs

**PRC 2 Volume 2 Financial Management Study Text and Question Bank were not present in the supplied upload set.** Add them to the local vault when available.

## PDF and privacy behaviour
The GitHub repository is public, so original ICAP study-text and question-bank PDFs are **not committed as public downloads**. The catalogue tracks which course files should be present. To open a PDF inside the site, use **Study → Study library → Import PDFs** and choose your own local copy. Imported PDFs are stored in browser IndexedDB on that device, not sent to GitHub.

Profile, topic checklist, mock history, mistakes and study sessions are stored in browser local storage. They do not sync between devices or users. Export a JSON backup periodically. Clearing site data may remove this information.

## Question-bank import
Subject IDs:
- `prc1-fa` — Financial Accounting
- `prc2-qm` — Quantitative Methods
- `prc2-fm` — Financial Management
- `prc3-bi` — Business Insights
- `prc3-eco` — Economics

The small built-in MCQ pool is explicitly labelled **illustrative demo content**, not official ICAP questions. Use the Mock page's JSON template and importer to add your own source-backed practice items. The Merit page produces a personal study report, not an official ICAP result or merit list.
