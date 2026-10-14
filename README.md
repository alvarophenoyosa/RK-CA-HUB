# RK | CA - HUB

A responsive CA-PRC study dashboard with a neon cyber interface, selectable themes, mock exams, subject progress, study utilities, one-click public PDF links, and an optional local PDF vault. It is a **single-file HTML MVP** with no package install or build step. This repository is public and the owner has confirmed permission to share the current course PDFs publicly.

## Themes
- **Neon Grid** — original dark cyber grid.
- **Jet Black Neon** — near-black canvas with cyan/magenta neon.
- **Clean White** — light, clean study workspace.
- **Old-School Classic** — paper-and-ledger inspired cream/forest palette.

Theme choice is saved in browser-local settings. Mock scores are colour-scaled from red through amber to green; subject coverage bars use separate subject colours.

## Publish with GitHub Pages
1. Open repository **Settings → Pages**.
2. Under **Build and deployment → Source**, choose **Deploy from a branch**.
3. Set branch to `main` and folder to `/(root)`, then save.
4. Open the **Actions** tab and watch the automatically created **pages build and deployment** workflow.
5. Once successful, open the published URL shown under **Settings → Pages**. For this repository it should be `https://alvarophenoyosa.github.io/RK-CA-HUB/`.

This site is static HTML/CSS/JavaScript, so the default GitHub Pages branch deployment is enough; no custom build workflow is required.

## Run locally
Download `index.html` and open it in a modern browser. For more reliable local PDF storage, use a local web server (for example, VS Code Live Server) and avoid private browsing mode.

## Current features
- HOME: study-time and streak metrics, subject coverage, recent mock attempts, and revision reminders.
- MOCK: timed one-question-at-a-time MCQ simulator, question navigation, score report, mistakes bank, and JSON question-bank import.
- STUDY: one-click hosted PDF catalogue grouped by official PRC subject and volume, optional browser-local PDF vault, topic tracker, mind-map workspace, formula references, interest/annuity calculators, and an illustrative Economics demand/supply plotter.
- PROFILE: student details, target date, topic coverage, study time, mock average, weak/strong subjects, and data export/import.
- MERIT: personal live progress report, subject performance table, and export.
- Four themes and score-dependent red → amber → green colours.

## PRC course PDF catalogue status
The Study catalogue lists these eight course PDFs, grouped by official subject and volume:
- **PRC 1 — Fundamentals of Accounting:** Study Text and Question Bank
- **PRC 2 — Quantitative Analysis for Business:** Study Text and Question Bank
- **PRC 3, Volume 1 — Business Insights:** Study Text and MCQs
- **PRC 3, Volume 2 — Economics:** Study Text and MCQs

According to ICAP's 2025 syllabus, the website now uses the three official PRC subjects: **PRC 1 — Fundamentals of Accounting**, **PRC 2 — Quantitative Analysis for Business**, and **PRC 3 — Business and Economic Insights**. PRC 2 covers Basic Mathematics, Financial Mathematics, Application of Statistics in Business, and Probability and Expected Values. PRC 3's Business Insights and Economics books remain separate catalogue volumes, but share progress and mock tracking under one subject.

## PDF and privacy behaviour
The Study catalogue provides one-click public links to the eight PDFs committed in this repository. The repository owner has confirmed that their permission covers public sharing of these study materials. Links point to files in the repository root and open in a new browser tab. The optional **Study → My personal study vault → Import personal PDFs** feature stores additional local copies in browser IndexedDB on that device.

Profile, topic checklist, mock history, mistakes and study sessions are stored in browser local storage. They do not sync between devices or users. Export a JSON backup periodically. Clearing site data may remove this information.

## Question-bank import
Subject IDs:
- `prc1-fa` — Financial Accounting
- `prc2-qa` — Quantitative Analysis for Business
- `prc3-bei` — Business and Economic Insights (both volumes)

Legacy progress and imported question data using `prc2-qm` or `prc2-fm` are normalised to `prc2-qa`; old `prc3-bi` and `prc3-eco` items are normalised to `prc3-bei` when the site loads.

**No MCQs are bundled with the site.** Placeholder/sample questions have been removed; the mock launcher remains disabled until a question bank is imported as JSON, so mock scores will only be based on imported items. Use the Mock page JSON template and importer to add source-backed practice items. The Merit page produces a personal study report, not an official ICAP result or merit list.
