## Cadence Privacy Policy & Data Usage

**Developer:** Winnie Mutunga
**Contact Email:** theselfstudy8@gmail.com
**Location:** Philadelphia, Pennsylvania, USA

Created: 18 January 2026
Last updated: 12 February 2026

---

### Quick Navigation
- [What is Cadence](#what-is-cadence)
- [Google OAuth & API Usage](#google-oauth--api-usage)
- [Google OAuth Scopes Used](#google-oauth-scopes-used)
- [Compliance With Google API Services User Data Policy](#compliance-with-google-api-services-user-data-policy)
- [OAuth Scope Justification](#oauth-scope-justification-for-verification)
- [Session Duration & Token Handling](#session-duration--token-handling)
- [How Cadence Protects Your Data](#how-cadence-protects-your-data)
- [Data Sharing & Third Parties](#data-sharing--third-parties)
- [No Sale of Data](#no-sale-of-data)
- [Data Retention & Deletion](#data-retention--deletion)
- [Your Rights as a User](#your-rights-as-a-user)
- [HIPAA Notice](#hipaa-notice)
- [Children's Privacy](#childrens-privacy)
- [Changes to This Policy](#changes-to-this-policy)
- [Contact & Support](#contact--support)

---

## What is Cadence?

Cadence is a privacy-first personal health logging application designed to help individuals better understand patterns in their body over time. Cadence does not maintain its own database or long-term server-side storage of user health data.

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

## Compliance With Google API Services User Data Policy
Cadence's use and transfer of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the Limited Use requirements.

## OAuth Scope Justification (For Verification)
Cadence requires read and write access to Google Sheets because:
  - Users may edit their data outside of Cadence directly in Google Sheets
  - Cadence must read the sheet to reflect those changes accurately
  - Syncing requires updating existing rows, not append-only access
  - Read-only access would prevent meaningful use of the app

This access is limited to:
  - The specific spreadsheet chosen by the user
  - The duration of the user's authenticated session (see [Session Duration & Token Handling](#session-duration--token-handling) below)

## Session Duration & Token Handling

When a user authenticates via Google OAuth, Cadence receives a short-lived access token. This token is:

  - **Stored in the browser's `sessionStorage`** — not in `localStorage`, cookies, or on any server
  - **Valid for up to 1 hour**, as defined by Google's OAuth token lifespan
  - **Automatically cleared** when the browser tab or window is closed, as `sessionStorage` does not persist across browser sessions
  - **Cleared after a successful sync** operation completes

Cadence does not refresh, extend, or silently renew OAuth tokens. When a token expires, the user must re-authenticate by clicking "Sync with Google Sheets" again.

In practical terms, a "session" in Cadence ends when **any** of the following occurs:
  - The OAuth token expires, as defined by Google
  - The user closes the browser tab or window
  - The sync operation completes and the token is cleared
  - The user disconnects their Google Sheet in Settings

Cadence does not store OAuth tokens on any server and does not maintain server-side sessions.

## How Cadence Protects Your Data

### Encryption in Transit
All communication between your browser and Google's APIs occurs over **HTTPS (TLS encryption)**. Cadence is hosted on Vercel, which enforces HTTPS for all connections. No data is transmitted in plaintext.

### Browser Storage
Cadence stores user data (entries, settings, saved filters) in the browser's `localStorage`. This data:
  - Remains on your device only
  - Is not transmitted to any Cadence server
  - Can be cleared at any time through the app's Settings page or by clearing your browser data

OAuth tokens are stored separately in `sessionStorage`, which is automatically cleared when the browser tab or window is closed.

### Token Handling
  - OAuth tokens are never stored on a server
  - Tokens exist only in the browser's `sessionStorage` for the duration of the authenticated session
  - Tokens are used solely to authorize read/write requests to the user's specific Google Sheet
  - Tokens are valid for up to 1 hour as defined by Google, and are not refreshed or renewed by Cadence
  - Cadence clears tokens after sync completion or when the browser session ends

### Input Security
  - All user text inputs are sanitized to prevent formula injection and cross-site scripting (XSS)
  - Character limits are enforced on all free-text fields
  - Rate limiting is applied to sync actions and form submissions

### No Background Data Collection
  - Cadence does not sync data in the background
  - Cadence does not collect behavioral or health analytics
  - OAuth is only triggered by explicit user action (clicking "Sync with Google Sheets")

## Data Sharing & Third Parties

Cadence does not share user health data with any third party. The following services are used in the operation of Cadence:

### Vercel (Hosting Provider)
  - **Purpose:** Hosts the Cadence web application and serves static assets
  - **Data processed:** Standard web request data (IP address, browser type) for site delivery and security, as handled by Vercel's infrastructure
  - **Analytics:** Vercel Analytics is enabled for basic, anonymous page-view metrics. No personal information or health data is included in analytics
  - **Vercel's privacy policy applies** to data processed by their infrastructure

### Google APIs (OAuth & Google Sheets API v4)
  - **Purpose:** Authenticates the user and reads/writes data to the user's own Google Sheet
  - **Data processed:** Only the health entries, settings, and filters that the user explicitly syncs
  - **All API calls are made directly from the user's browser** to Google's servers — Cadence does not proxy or intercept this data

### Google Apps Script (Contact Form)
  - **Purpose:** The contact form at `https://cadence-olive.vercel.app/contact` sends messages to a Google Apps Script, which delivers the submission as an email to the developer and logs it in a private Google Sheet for record-keeping
  - **Data collected:** Name, email address, and message content — submitted voluntarily through the contact form only
  - **Data storage:** Submissions are recorded in a Google Sheet accessible only to the developer. This is used solely to track and respond to support inquiries. No health data is collected through this form
  - **This is the only data that leaves the user's browser and passes through a Cadence-controlled server route** (`/api/contact`), and it is forwarded immediately to the Google Apps Script without being stored on Cadence's server

### Services Cadence Does NOT Use
  - No advertising networks
  - No data monetization services
  - No third-party data processors beyond those listed above
  - No social media tracking or pixels
  - No customer data platforms
  - No AI or machine learning services applied to user data

## No Sale of Data

Cadence does not sell, rent, trade, or monetize user data.

No user data — including health entries, settings, Google account information, or contact form submissions — is sold to or shared with third parties for commercial purposes. Cadence has no advertising relationships, data broker partnerships, or revenue derived from user data.

## Data Retention & Deletion

### Local Browser Data
Local data (entries, settings, saved filters) is stored in your browser's `localStorage` and can be deleted at any time by:
  - Using the "Advanced Options" section in Cadence Settings to reset or delete app data
  - Clearing your browser's storage/cache directly

### Google Sheets Data
Google Sheets data can be deleted by:
  - Disconnecting from within Cadence Settings (removes Cadence metadata from the sheet)
  - Permanently deleting the spreadsheet from your Google Drive

Cadence does not retain copies of your Google Sheets data.

### Contact Form Submissions
Messages submitted through the contact form are forwarded via Google Apps Script to the developer's email and logged in a private Google Sheet accessible only to the developer. This log is maintained solely for the purpose of tracking and responding to support inquiries. Cadence's server route (`/api/contact`) forwards the submission immediately and does not store it on the server itself. Users may request deletion of their contact form submissions at any time by [emailing the developer](#contact--support).

### Server-Side Logs
  - **Vercel function logs:** Vercel may retain logs for serverless function invocations (the `/api/contact` route) as part of its standard infrastructure. These logs may include request metadata such as timestamps and IP addresses. Cadence does not intentionally log or store health data in server logs. See [Vercel's data retention policies](https://vercel.com/docs/security) for details
  - **Vercel Analytics:** Anonymous page-view data is collected by Vercel Analytics. This does not include personal information or health data
  - **Cadence does not implement custom server-side logging** of user activity, health data, or API errors beyond what Vercel provides by default

### What Cadence Does Not Retain
  - No health data on any server
  - No OAuth tokens beyond the browser session
  - No user account records (Cadence does not have user accounts)
  - No copies of synced Google Sheets data

## Your Rights as a User

### Revoke Google Access
You may revoke Cadence's access to your Google Sheet at any time by visiting [Google Account Permissions](https://myaccount.google.com/permissions) and removing Cadence.

### Delete Your Data
  - **Browser data:** Use "Advanced Options" in Cadence Settings or clear your browser storage
  - **Google Sheets data:** Delete the spreadsheet from Google Drive or remove Cadence's data from within the sheet
  - **Contact form submissions:** You may request deletion of any contact form messages by emailing theselfstudy8@gmail.com

### Export Your Data
  - You can export your data directly from Cadence as a **CSV** or **PDF** at any time
  - You can access your data directly in your Google Sheet, which you own and control

### Request Information
You may contact us at any time to ask what data, if any, Cadence holds related to you. Given Cadence's architecture, the answer in most cases is: none — your data lives in your browser and your Google Sheet.

## HIPAA Notice
Cadence is not a HIPAA-covered entity and does not claim HIPAA compliance.
Cadence is a personal health tracking tool and does not aim to replace or provide medical advice, diagnosis, or treatment.

## Children's Privacy
Cadence is not intended for use by individuals under the age of 18.

## Changes to This Policy
This policy may be updated as Cadence evolves.
Significant changes will be reflected by an updated "Last updated" date.

## Contact & Support

For privacy inquiries: theselfstudy8@gmail.com
For general support: theselfstudy8@gmail.com

You can also reach us through the app: `https://cadence-olive.vercel.app/contact`