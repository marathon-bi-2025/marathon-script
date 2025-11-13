📌 Google Apps Script Repository for Marathon Myanmar

This repository contains multiple Google Apps Script projects used across various departments in Marathon Myanmar (BI, Sales, Finance, HR, Tech, etc.).
Each project is linked to a specific Google Sheet, and version-controlled using clasp and GitHub for reliable development, backups, and collaboration.

🚀 Features

Centralized codebase for all Marathon Apps Script projects

Version control using Git & GitHub

Clasp-enabled syncing between local code and Google Apps Script

Organized project structure (one folder per sheet)

Supports automation tasks: KPI processing, cleaning, reporting, validation, dashboard prep, API integrations, triggers, etc.

📁 Repository Structure
/marathon-apps-scripts/
  sheet_sales_report/         # Apps Script for Sales reporting automation
  sheet_finance_dashboard/    # Apps Script for finance calculations & KPIs
  sheet_hr_kpi/               # HR KPI automation (attendance, SLA, submissions)
  sheet_operations_tools/     # Operational scripts, POS/ERP data processing
  ...


Each folder contains:

.clasp.json – Clasp project config

Code.gs / .js / .ts – Script files

appsscript.json – Project manifest

🛠️ Setup Instructions

Below is the standard way to clone, edit, and deploy Apps Script projects using clasp.

1. Install Node.js & clasp
npm install -g @google/clasp


Login with your Google account:

clasp login


Enable Apps Script API (if needed):
https://script.google.com/home/usersettings

🔗 Cloning an Apps Script Project

Each project in this repo corresponds to a Google Sheet script with a unique SCRIPT_ID.

To clone one project:

mkdir <project-folder>
cd <project-folder>
clasp clone <SCRIPT_ID>


This pulls all Google Apps Script files into the folder.

🔄 Sync Workflow
Pull changes from Google Apps Script → Local
clasp pull

Push local changes → Google Apps Script
clasp push

💡 Recommended Workflow for Multiple Sheets

Each Google Sheet should have its own folder.

Example:

marathon-apps-scripts/
  kpi_daily_snapshot/
  sales_invoice_auto/
  hr_submission_monitor/
  finance_profitability/


Inside each folder:

Run clasp pull before editing locally

Run clasp push after changes

Commit and push to GitHub

🧭 Git Commands

Initialize repo:

git init


Add remote:

git remote add origin https://github.com/marathon-bi-2025/marathon-script.git


Push:

git add .
git commit -m "Update project"
git push -u origin main

⚠️ Common Errors
"project file already exists"

Occurs if .clasp.json exists in the folder.

Fix:

Windows:

del .clasp.json


Or use an empty folder before running clasp clone.

📌 Notes

This repo contains only script code — spreadsheet data stays in Google Sheets.

Sensitive credentials should not be stored in this repo.

Use environment variables or Script Properties for API keys.

🧑‍💻 Maintainer

Than Soe Aung (Marathon BI)
Email: thansoeaung@marathonmyanmar.com
