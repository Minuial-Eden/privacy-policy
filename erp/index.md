---
title: ERP Extension - Privacy Policy
---

# Privacy Policy — ERP

**Last updated: 17 July 2026**

## The short version

There is no server. There is no account. There is no analytics, no
telemetry, and no tracking of any kind. Nothing this extension sees about
your loads, your emails, your messages or your customers is sent to us,
because there is no "us" to send it to — nobody is on the other end.

It's a set of shortcuts that runs entirely inside your own browser, on pages
you've already opened and are already logged into. It has no interest in your
business, and it isn't built to learn anything about it.

## What it can see

To do its job the extension reads the pages you're on:

- **erp.gologity.com** — load numbers, stops, times, broker and team-member
  names, so it can write your comments, build a Bill of Lading, and know
  which load you right-clicked.
- **mail.google.com** — enough to open a search, expand a thread, or insert
  text where your cursor is.
- **web.telegram.org** — enough to put a load number in the search box, or a
  message in the message box.

All of that happens in your browser and stays there. It's read, used, and
forgotten.

## What it stores, and where

Everything below lives in your own browser's extension storage. None of it is
uploaded anywhere by us.

| What | Where | Why |
|---|---|---|
| Your feature toggles and dispatcher name | `chrome.storage.sync` | So the extension behaves the way you set it up |
| A cached copy of the shared contact list | `chrome.storage.local` | So broker lookups work without re-fetching |
| A diagnostic log (~2000 recent entries) | `chrome.storage.local` | So a bug can be diagnosed after it happens |

Two things worth being straight about:

- **The diagnostic log contains real work data** — load numbers, lanes,
  broker names — because that's exactly what makes it useful when something
  breaks. It never leaves your machine. You can read it, copy it, or wipe it
  whenever you like: right-click the extension icon → **Options**. Clearing
  it is one button.
- **Settings use Chrome's own sync.** If you have Chrome Sync switched on,
  Chrome copies your toggles and dispatcher name to your Google account, the
  same way it syncs your bookmarks. That's Chrome's mechanism and Google's
  policy, not ours — we just use the normal settings API. Nothing else the
  extension touches goes through it.

## What leaves your browser

Two things, and neither carries anything about you:

1. **The shared contact spreadsheet.** Every 30 minutes the extension reads
   the Google Sheet your team publishes, to keep broker names and Telegram
   links current. It's a plain read. Nothing is sent up.
2. **One example image.** The "P⦿D Circle Request" feature inserts a sample
   photo hosted at `postimg.cc` into your email so the carrier can see what
   you're asking for. Your browser — and later your recipient's — loads that
   image from postimg.cc, which means postimg.cc sees a request for it, the
   same as any image in any email. Nothing about you or the load is included.

Opening Gmail or Telegram is just your browser going to Gmail or Telegram,
exactly as if you'd typed the address yourself.

## The AutoHotkey companion

The extension ships with an optional AutoHotkey script for the Zoom desktop
app. If you install and run it, it **watches your clipboard**, so that copying
a phone number can bring Zoom up and dial it. That check happens on your own
PC, inside that script, and nothing is recorded or sent anywhere. It also
keeps a small log file next to itself, on your machine.

If you'd rather nothing watched your clipboard, don't run it — the browser
features work fine without it.

## What we don't do

- We don't collect, store, or transmit your data.
- We don't sell or share anything, because we don't have anything.
- We don't use any third-party analytics, advertising, or tracking service.
- We don't ask you to sign in or create an account.
- We don't read your clipboard from the extension.

## Removing everything

Uninstalling the extension removes its stored data with it. To clear the
diagnostic log without uninstalling, use **Options → Clear**. To remove the
AutoHotkey script, close it and delete its folder.

## Changes

If any of this ever stops being true, this page changes first. The date at
the top is when it last did.

## Contact

Questions go to whoever on your team set this up for you.
