## Cadence Privacy Policy & Data Usage
Created: 18 January 2026
Last updated: 12 February 2026

## What is Cadence?

Cadence is a privacy-first personal health logging application designed to help individuals better understand patterns in their body over time. Cadence does not operate its own backend, database, or servers for storing any data.

Your data remains under your control at all times.

## Google OAuth & API Usage
Cadence uses Google OAuth only when you explicitly choose to sync your data with Google Sheets.

OAuth is required to:
  - Write your entries and settings to your Google Sheet
  - Read your Google Sheet to display dashboards and insights

OAuth is *not* triggered:
  - Automatically
  - On every entry
  - Without user action

You may disconnect your Google Sheet at any time through Settings with a single click.

## Google OAuth Scopes Used
Cadence requests the following Google API scope:
`https://www.googleapis.com/auth/spreadsheets`

### Why this scope is required

This scope is necessary to:
  - Create structured health logs in your selected Google Sheet
  - Update existing rows when syncing changes
  - Read previously synced data to generate summaries and insights
  - Restore data and settings preferences if you return to Cadence on another device

Cadence **does not**:
  - Access spreadsheets you have not explicitly connected
  - Read unrelated files or contents
  - Share spreadsheet data with third parties

## OAuth Scope Justification (For Verification)
Cadence requires read and write access to Google Sheets because:
  - Users may edit their data outside of Cadence directly in Google Sheets
  - Cadence must read the sheet to reflect those changes accurately
  - Syncing requires updating existing rows, not append-only access
  - Read-only access would prevent meaningful use of the app

This access is limited to:
  - The specific spreadsheet chosen by the user
  - The duration of the user’s authenticated session

## How Cadence Protects Your Data
Cadence implements multiple safeguards:
  - No persistent OAuth token storage
  - OAuth is requested on-demand only
  - Rate-limited sync actions
  - Input sanitization to prevent formula injection
  - Length restriction on all free-text fields
  - No third-party analytics or trackers
  - No background data syncing

Cadence is designed so that loss of access to Cadence does not result in loss of data, provided an up-to-date synced Google Sheets.

## Data Retention & Deletion
Local data can be deleted by clearing browser storage. These settings can be found under "Advanced Settings"

Google Sheets data can be deleted by:
  - Disconnecting from within Cadence settings
  - Permanently deleting the spreadsheet from your Google Drive.
  
Cadence has no ability to delete or retain data on your behalf

## HIPAA Notice
Cadence is not a HIPAA-covered entity and does not claim HIPAA compliance.
Cadence is a personal health tracking tool and does not aim to replace or provide medical advice, diagnosis, or treatment.

## Children’s Privacy
Cadence is not intended for use by individuals under the age of 18.

## Changes to This Policy
This policy may be updated as Cadence evolves.
Significant changes will be reflected by an updated “Last updated” date.

## Contact & Support
Contact us from [within the app here](https://cadence-olive.vercel.app/contact)!
