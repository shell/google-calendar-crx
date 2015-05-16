Google Calendar Join Link Opener for Chrome
===========================================

This solution is fork of [Google Calendar for Chrome](https://github.com/manastungare/google-calendar-crx) repurposed for opening "join meeting" links automatically 1 minute before meeting starts

## Problem

When you having a lot of meetings in your calendar, it's pain everytime to open up calendar app and search for join link in the event description / location / title.


## Installation

  1. Clone this repo
  2. In Chrome settings click following ![Install extension](assets/add_extension.png?raw=true)
  3. Point it to **/src** directory of the folder
  4. Authorize with your google account

## If you using another(company) account for calendars

  1. Click on Account button on top-right of the browser window
  2. Switch to person -> Add Person
  3. Enable Google Calendar extension and go through authorization process again
  4. Open up extension -> settings and click "Reveal auth token"
  5. Copy and paste token to `/src/background.js` at line 26

    `background.CUSTOM_AUTH_TOKEN = 'YOUR TOKEN HERE';`

  6. Click "Reload" on the Google Calendar in Extensions settings.


Extension updates your event list every 15 minutes and opens up Join link 1 minute before a meeting.

You can hide button from the toolbar, it still will be working in background as long as extension is enabled.
