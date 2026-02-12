# Quick Navigation
### General Questions
- [What is Cadence](#what-is-cadence)
- [Who is Cadence for](#who-is-cadence-for)
- [Where is my data stored ](#where-is-my-data-stored)
- [HIPAA Compliance](#is-cadence-hipaa-compliant)
- [Google Sheet Access](#does-cadence-have-access-to-my-google-sheet)
- [Can I lose my data](#can-i-lose-my-data)
- [Do I need an account](#do-i-need-to-use-an-account-to-use-cadence)
- [Why is Cadence built this way](#why-is-cadence-built-this-way)

### App FAQ
- [How to start using Cadence](#where-do-i-start)
- [Cadence modes](#what-are-these-modes)
- [Connecting a Google Sheet](#how-do-i-connect-a-google-sheet)
- [Restore from Google Sheet to Cadence](#how-do-i-restore-my-stuff)
- [Downloading data via CSV](#i-want-to-download-my-data-as-a-csv-file)
- [Downloading data via PDF](#i-want-to-download-my-data-as-a-pdf)

### Troubleshooting
- [Google Sheet isn't syncing](#my-google-sheet-isnt-syncing)
- [Sync buttons aren't working](#im-clicking-the-sync-buttons-but-im-getting-an-error)
- [Resetting settings but save entries](#i-want-to-reset-all-of-my-settings-but-save-my-entries)
- [I want to leave Cadence](#i-want-to-leave-cadence)
- [Contact us](#contact-us)

# General Questions
## What is Cadence?

Cadence is a privacy-first personal health logging app designed to help individuals better understand patterns in their body over time. Cadence does not operate its own backend, database, or servers for storing any data.

## Who is Cadence for?
Cadence is for anybody who has ever said "that's new, I've never had [insert symptom here]" or "huh. I wonder if these things are related somehow". Cadence helps bring awareness to your bodily cycles, how they can potentially relate to each other, and even helps compare week-to-week and month-to-month data. 

## Where is my data stored?
Depending on how you use the app, your data is stored either:
- *Locally in your browser*, or
- *In your own Google Sheet*, which you control

> ℹ See the [What are these modes](#what-are-these-modes) FAQ for more information

Cadence has and will never:
- Store your health data anywhere other than your authorized and linked Google Sheet
- Keep copies of your entries
- Sync your entries outside of your browser or your linked Google Sheet
- Back up your entries elsewhere

## Is Cadence HIPAA Compliant?
Cadence is **not** a HIPAA-covered service.
HIPAA applies to healthcare providers, health plans, and their contracted service providers. Cadence does not act as a healthcare provider, does not store your health data on its servers, and does not receive or manage protected health information on your behalf.
Your data is stored either:
- Locally in your own browser, or
- In your personal Google Sheet, which you control

> ℹ See the [What are these modes](#what-are-these-modes) FAQ for more information

Because Cadence does not collect, transmit, or retain your health data, HIPAA compliance does not apply in the traditional sense.
That said, Cadence is intentionally designed to follow HIPAA-aligned principles, including:
- Data minimization
- User-controlled storage
- No secondary use of data
- No advertising or tracking
> ℹ If you are required to use a HIPAA-compliant system for diagnosing, medical, or clinical purposes, Cadence may not be an appropriate tool for you.

## What about privacy?
Please see [our policy](./index.md) to learn more about Cadence's privacy policy and data usage

## Does Cadence have access to my Google Sheet?
**Yes,** but within context. 
Cadence only accesses your Google Sheet when you explicitly click "Sync with Google Sheets" or perform a restore.

When connected:
- Access happens directly from your browser; authorization is requested each time.
- Data is written **only** when you click a "Sync with Google Sheets" button.
- You can revoke access at any time from your Google account.
> ⚠️ Note: Removing your sheet from Cadence disables syncing, but does not revoke authorization in your Google account. 
> If you’d like to completely revoke Cadence’s access to your sheet, you can do so from your Google Account at [https://myaccount.google.com/permissions](https://myaccount.google.com/permissions).

## Can I lose my data?
**Yes.** If you choose local-only storage “Anonymous Mode”:
- Clearing your browser data **will** remove your entries
- If your browser crashes, entries *may be* lost
- Using a different device **will not** carry data over

> ℹ We recommend connecting a Google Sheet if you’d like an easier time switching devices or seeing all your data. Please see our [How do I connect a Google Sheet](#how-do-i-connect-a-google-sheet) FAQ.

## Do I need to use an account to use Cadence?
**No.**
You can use Cadence without signing in with an account. This is known as “Anonymous Mode” in the app. In Anonymous Mode, data is stored only on your current device.
If you choose to sign in and connect a Google Sheet, you can access your data across devices, but you’ll need to reconnect your sheet on each new device. If you saved your settings, those will also be retained via the Google Sheet and can be restored on your new device.
> ⚠️ **Please Note**: If you clear your browser history, switch to a different device or browser, or if your preferred browser crashes, **your data may not be retained**. It's always recommended to download a CSV of your data prior to clearing your browser history, switching devices, or updating your browser. Please see our [Can I lose my data](#can-i-lose-my-data) and [I want to download a CSV](#i-want-to-download-my-data-as-a-csv-file) FAQs for more information on tradeoffs with using Anonymous Mode and downloading your data from the app.

## What data does Cadence collect?
The hosting provider may temporarily process standard web request information (such as IP address and browser type) for basic site delivery and security.
Cadence collects no health data, no tracking data, and no behavioral analytics.

## Why is Cadence built this way?
Cadence is designed around a simple idea:
Your data belongs to you. *Always.*

# App FAQ

## What are these modes?
Cadence operates in two distinct ways. 
1. **Signed In & Synced Mode** - This is the mode name if you have a Google Sheet linked to Cadence. Each time you click one of the "Sync with Google Sheets" buttons around the application, Cadence will push all of your current entries, settings, and saved filters into your Google Sheet for safe storage, and also pull any data from the sheet to make sure everything is up to date. You can forego syncing for 48 hours until you're prompted by the UI to sync. *This is the recommended way of using Cadence as this secures your data and ensures your data is safely synced outside of your browser regardless of whether you clear your history or switch to a new device*. 
2. **Anonymous Mode** - This is the mode name if you'd rather not link a Google Sheet. All of your data will be stored in your current device's browser. There are some tradeoffs to be made aware of when using this mode. Please visit [Can I lose my data](#can-i-lose-my-data) FAQ for more information.

## Where do I start?
When you first visit Cadence, you will be navigated to the landing page. Click "Get Started" when you've read through what you can do with Cadence.
You'll be given 2 options:
- **Signed In & Synced Mode** - If you want to start off with a Google Sheet so that you don't have to set it up later, click this option. This means that all of your entries, settings, and filters will be backed up to that Google Sheet.
> ℹ Make sure that you are the editor of the Google Sheet you'd like linked. That is the account you'll select in popups to authorize Cadence to read to and write from the Google Sheet to save your entries and settings.

> ℹ If you are returning to Cadence with a Google Sheet that already has entries, see our [How do I restore my stuff](#how-do-i-restore-my-stuff) FAQ.

- **Anonymous Mode** - If you want to start off without adding a Google Sheet, click this option. This means that all of your entries, settings, and filters will be kept on the current device you're on.
  
> ⚠️ **Please Note**: It's recommended to connect a Google Sheet in the case that your browser crashes, or if you clear your browsing history often. Not doing so can cause data loss. Please see the [Can I lose my data](#can-i-lose-my-data) FAQ for more information.
  
> ℹ You will always have the option of adding a Google Sheet later if you'd like. Please see the [How do I connect a Google Sheet?](#how-do-i-connect-a-google-sheet) FAQ for more information.

After selecting one of the modes, click the "Continue to Settings" button to continue.

## How do I connect a Google Sheet?
1. Navigate to the Dashboard by clicking the gear icon on the top right of the page.
2. Locate the "Google Sheets Integration" section. Here, you'll have a space to copy and paste your preferred blank Google Sheet.
3. Click the "📊 Connect a Google Sheet" button, then "Continue" on the popup.
> ℹ If you've made a mistake after connecting the Google Sheet, click either the "Edit" button to edit the URL. If you want to disconnect and try again, click the "Disconnect" button.
4. Scroll to the bottom of the Settings page and click the "Sync with Google Sheets" button to complete the first sync. 

## How do I restore my stuff
If you have a Google Sheet with entries and: 
  - returning to Cadence or
  - switching from one device to another

Then, welcome back! Here are steps to restore your data to Cadence:
- On the Welcome page, click "Get Started".
- A popup will show and within the first option "Signed In & Synced Mode", you should see the "Already set up?" highlighted section. Click "restore your settings and entries here" hyperlink. 
- Add your Google Sheet URL to the textbox and then click "Sign In with Google & Restore". 
> ℹ You will be prompted to authorize with your account. Please select the same account that your Google Sheet was created with. 
- Cadence will automatically begin restoring your entries, settings, filters, and even the name of your Google Sheet. When restoration is complete, you’ll be routed to the dashboard and ready to make new entries.

## I want to download my data as a CSV file
If you have entries and would like to download your data, do the following steps:
1. Click the three horizontal line menu on the top left of the application. History is the last button under the "Views" section
2. Locate the blue "Export CSV" button on the upper right of the page, which will download all of your data. This will automatically start the CSV download to your current device which you can store anywhere.
> ℹ If you're not seeing all of your data, please make sure that the "Show" filter is set to "All Time". 

> ℹ If the "Export CSV" button is unclickable, it means you have yet to make any entries, or the time frame you've chosen has no data. Try expanding your date filters or begin by adding an entry. 

## I want to download my data as a PDF
If you have entries and would like to download your data as a PDF, do the following steps:
1. Click the three horizontal line menu on the top left of the application. PDF Export is the first button under the "Reports" section.
2. Select what report period you'd like to see in your PDF (click "All Time" for all data), and which categories you'd like to export to PDF. 
3. Scroll down and then click "Generate PDF". This will automatically start a download from the app to your device with the current date.

> ℹ If the "Generate PDF" button is unclickable, it means you have yet to make any entries.

> ℹ If you have generated a PDF but don't see any data, it may mean that the time frame or categories you have selected have no data.

# Troubleshooting
## My Google Sheet isn't syncing
If you're not seeing recent entries show up in your Google Sheet, it may be an error in how Cadence is trying to write the information. Try the following steps:
1. Refresh the page and click any "Sync with Google Sheets" button around the app. 
2. Relink the sheet:
  - Navigate to Cadence Settings by clicking the gear icon on the top right of the page.
  - Find the "Google Sheets Integration" section at the top of the page.
  - Double check that Cadence still has your preferred Google Sheet linked. If not, please link it, then scroll to the bottom of the page and click the "Sync with Google Sheets" button. 

> ℹ If it's still not working, please [contact us](#contact-us) with a screenshot of any errors and details on what happened and we'll do our best to fix it.

## I'm clicking the Sync buttons but I'm getting an error
If you're clicking the sync buttons but it's giving you an error, you may be attempting to log in with the incorrect Google Account. Please make sure that the Google Account you have your Google Sheet set up with is the same one you're using to sign in. 

> ℹ If it's still not working, please [contact us](#contact-us) with a screenshot of the error and details on what happened and we'll do our best to fix it.

## I want to reset all of my settings but save my entries
If you'd like to reset all of your settings, it's as easy as scrolling to the bottom of the Settings page and clicking "Advanced Options".
- **Anonymous Mode** - If you would like to permanently leave Cadence and *don't* have a Google Sheet linked (aka "Anonymous Mode"), clicking "Reset App Settings Only" will clear all of your settings, saved filters, and app preferences. Your entries will remain safe in your browser storage.
- **Signed in & Synced Mode** - If you would like to permanently leave Cadence and you *do* have a Google Sheet linked, clicking "Reset App Settings Only" deletes the saved settings and filters from your Google Sheet. Your current Google Sheet and all data will be retained.

> ℹ If you'd like to leave Cadence entirely, please see the [I want to leave Cadence](#i-want-to-leave-cadence) FAQ.

## I want to leave Cadence
While we're sad to see you leave, we believe all visitors have this right and have tried to make it as easy as possible to leave the app. Simply navigate to the Cadence Settings page and click "Advanced Options" at the very bottom.
- **Signed in & Synced Mode** – To permanently leave Cadence with a Google Sheet linked, click **Delete Device and Sheet Metadata**. This removes all Cadence metadata from your Google Sheet and disables syncing for new entries. Your previously synced entries remain in the sheet. You’ll be asked to authorize deletion once more; be sure to click through both popups before navigating away.
- **Anonymous Mode** – To permanently leave Cadence without a linked Google Sheet, click **Delete All Data**. This removes all locally saved data (entries, settings, filters) permanently. To save your data first, download it as a CSV or PDF.
  
> ⚠️ **Please Note**: If you don't have a Google Sheet linked, all of your data will be removed from the application and your device **permanently**. If you'd like to download and save your entries to a CSV, please see the [I want to download my data as a CSV](#i-want-to-download-my-data-as-a-csv-file) or [I want to download my data as a PDF](#i-want-to-download-my-data-as-a-pdf) FAQs.

# Contact us
### Have more questions, or not finding what you're looking for? 
Contact us from [within the app here](https://cadence-olive.vercel.app/contact)!

