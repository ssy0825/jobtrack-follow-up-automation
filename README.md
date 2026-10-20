# JobTrack — Automated Job Follow-up Reminder

A personal workflow automation project built with **n8n, JavaScript, CSV, and SMTP**.
<img width="1621" height="362" alt="workflow-overview" src="https://github.com/user-attachments/assets/1c5e235d-8a95-4d97-9470-0372257b963d" />

## Overview

JobTrack automates follow-up reminders for job applications. It reads application records from a local CSV file, identifies overdue follow-ups, sends email reminders, and updates the corresponding records to prevent duplicate notifications.

This project demonstrates practical workflow automation, data processing, conditional logic, and email integration.

## Problem Statement

Tracking job applications manually can be repetitive. Without a reliable reminder system, it is easy to overlook follow-up dates or send duplicate reminders.

## Solution

JobTrack automates the follow-up process:

1. Read job application records from a CSV file.
2. Identify applications whose follow-up dates are due or overdue.
3. Check that the follow-up status is `Pending` and a reminder has not already been sent.
4. Send an email reminder through SMTP.
5. Update the corresponding records to mark reminders as `Sent`.
6. Convert the updated records back to CSV and save the file.

## Tech Stack

- **n8n** — Workflow orchestration and scheduled execution
- **JavaScript** — Filtering, data normalization, and record updates
- **CSV** — Local data storage
- **SMTP** — Email notifications
- **Docker** — Local development environment

## Workflow

`Schedule Trigger → Read CSV → Extract Records → Filter Due Follow-ups → Prepare Email → Send Email → Update Records → Convert to CSV → Write CSV`

A manual trigger is also available for testing.

## Key Features

- Scheduled follow-up checks
- Conditional filtering based on follow-up date and status
- Automated email notifications
- CSV record updates
- Duplicate reminder prevention using a `Follow-up Sent` field
- Manual execution for testing and troubleshooting

## Testing

The workflow was tested with sample job application records. The email notification and CSV update process were verified.

## Limitations

- Uses a local CSV file rather than a database.
- Requires the local n8n environment to be running for scheduled execution.
- Email delivery depends on the configured SMTP service.
- If some emails are sent but a later step fails, records may need to be reconciled before retrying.

## Future Improvements

- Add more robust error handling and retry logic.
- Record the timestamp of each reminder.
- Add a dashboard for tracking applications and interviews.
- Integrate with a spreadsheet or database.
- Explore AI-assisted application categorization or follow-up message drafting.

## Project Status

**Working MVP — tested end to end.**
<img width="410" height="340" alt="image" src="https://github.com/user-attachments/assets/9dd754e3-926f-484d-9158-9bf97a73cf6e" />


This is a self-initiated portfolio project, not a client engagement.
