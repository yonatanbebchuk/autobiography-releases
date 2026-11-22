# Autobiography

A private record of the people in your life and the events you shared with them. It is built on your own Mac from your contacts and calendars, and kept on your devices and in your own iCloud.

This repository holds the Mac app's downloads and the feed the app updates itself from. The source is not public.

Autobiography is in beta, for invited testers. Expect rough edges, and tell me about them.

## What you need

- A Mac on macOS 26 or later.
- Optional: iCloud signed in on the Mac, to have the same record on your iPhone. The iPhone app comes through TestFlight, by invitation.
- Optional: a Google account, for your Google contacts and calendars. During the beta, Google sign-in works only for addresses I have added, so tell me which one you will use.

## Install

1. Download [Autobiography.zip](https://github.com/yonatanbebchuk/autobiography-releases/releases/latest/download/Autobiography.zip). Earlier builds are under [Releases](https://github.com/yonatanbebchuk/autobiography-releases/releases).
2. Double-click the zip and drag **Autobiography** to your Applications folder.
3. Open it. The app is signed with an Apple Developer ID and notarized by Apple, so macOS opens it without a warning. It asks for Contacts and Calendars, which it reads to build the record and never writes to, and for your location, which it keeps only as a country and a city.
4. Leave it running. It keeps the record current in the background, with or without a window.

## Updates

The app looks for a newer build every hour and downloads it by itself. **Settings › General › Updates** says which build you have and what is so. A downloaded build goes in when you press **Relaunch to update**, when you quit the app, or by itself once the Mac has been left alone for ten minutes.

Every build is signed, and the app installs only builds signed with the key it was made with. The updater is [Sparkle](https://sparkle-project.org), which is open source.

Leave **Builds** on Tested. Updates are not optional for long: a build that changes the record's format makes older copies stop syncing until they update, and the app says so when that happens.

## Connecting an assistant

Optional, and off until you turn it on. **Settings › Assistants** lets Claude read your record and, if you allow it, change it. The page walks through what it needs.

## Your data

The record lives on your Mac, in `~/Library/Application Support/Autobiography`, and in the private database of your own iCloud account when iCloud is on. I run no server for this app, I do not receive your data and I cannot see it. The app has no analytics, advertising or tracking.

What the app talks to: Apple, for iCloud and to turn your location into a city; Google, only if you sign in; GitHub, to look for a newer build; and whatever you connect yourself.

The full statement is the [privacy policy](https://yonatanbebchuk.com/projects/autobiography/privacy), which the app also links from **Settings › General**.

To remove everything: quit the app, delete it from Applications, and delete `~/Library/Application Support/Autobiography`.

## Problems

Open an issue here: [Issues](https://github.com/yonatanbebchuk/autobiography-releases/issues). Say what you did, what you expected and what happened, with your macOS version and the build from **Settings › General › Updates**. A screenshot helps.
