# Job Opportunity Finder (n8n)

Automated workflow that finds Business Analyst jobs every day, scores
them against my profile, logs them to Google Sheets, and emails me the
best matches.

![Workflow](docs/workflow-screenshot.png)

## How it works
1. Schedule Trigger runs daily at 9 AM IST
2. Fetches jobs from the Himalayas API
3. Splits and normalizes job records
4. Filters for target job titles
5. Scores each job against my skills (JavaScript Code node)
6. Appends or updates rows in Google Sheets
7. Sends a summary email via Gmail

## Setup
1. Install n8n (cloud or self-hosted)
2. Import `workflow.json` (Workflows → Import from File)
3. Connect your own Google Sheets and Gmail credentials
4. Replace `YOUR_SHEET_ID` and `YOUR_EMAIL` in the nodes
5. Publish the workflow

## Tech
n8n, JavaScript, REST APIs, Google Sheets API, Gmail API

## Roadmap
- [ ] Add more job sources
- [ ] Deduplicate against the sheet
- [ ] LLM-based job-fit scoring
- [ ] Error-alert workflow
