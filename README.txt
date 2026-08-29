FSTD Instructor Log — iPhone deployment
=======================================

Everything here is static. No build step, no server code.

PUBLISH (from the Mac mini, once)
1. github.com -> New repository -> name it e.g. "fstd-log" -> Public -> Create.
2. On the repo page: "Add file" -> "Upload files" -> drag in ALL files from this
   folder (index.html, sw.js, manifest.webmanifest, icon-180.png, icon-512.png)
   -> Commit changes.
3. Settings -> Pages -> Source: "Deploy from a branch", Branch: main / root -> Save.
4. Wait ~1 minute. Your URL is:
      https://<your-github-username>.github.io/fstd-log/

INSTALL ON THE IPHONE (once)
5. Open that URL in Safari on the iPhone.
6. Share button -> Add to Home Screen -> Add.
7. Open it from the Home Screen. It runs full screen, works with no signal
   (the service worker caches it), and survives iOS updates — nothing is signed,
   nothing expires, no App Store involvement.

DAILY USE
- Record sessions on the phone. Entries are stored on the phone.
- Settings -> "Save to iCloud Drive" writes FSTD-log-data.json via the share
  sheet: choose "Save to Files" -> iCloud Drive -> your logbooks folder.
- The Mac version opens that same file. Same format, both directions.
- Settings -> "Load from iCloud Drive" pulls the Mac's file onto the phone.

UPDATING LATER
- Replace index.html in the repo with a new build and commit. The phone picks up
  the new version next time it has signal; your logged entries are untouched.

NOTE ON PRIVACY
- Static hosting is public. The app file contains no personal data: your name,
  licence numbers and log entries live only on your devices and in your iCloud
  Drive file. If you'd rather not use a public repo, any private static host
  with an https URL works identically.
