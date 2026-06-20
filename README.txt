BATTLE PLAN — HOW TO GET A REAL ANDROID APK
=============================================

You have a complete installable web app here (index.html, manifest.json,
service-worker.js, icons/). To turn it into a real .apk you can install
on your phone, do this (free, ~10 minutes, no coding):

STEP 1 — Host the files online (so PWABuilder can read them)
--------------------------------------------------------------
Easiest free option: GitHub Pages.

1. Go to github.com and create a free account if you don't have one.
2. Create a new repository, e.g. "battle-plan".
3. Upload ALL files in this folder (index.html, manifest.json,
   service-worker.js, and the icons folder with both PNGs) — keep the
   same folder structure (icons/icon-192.png, icons/icon-512.png).
4. Go to the repo's Settings -> Pages -> set Source to "main" branch,
   root folder. Save.
5. GitHub gives you a URL like:
   https://yourusername.github.io/battle-plan/
   Open it and confirm the app loads correctly in your phone browser.

(Alternative: Netlify or Vercel also host static sites free and are
just as easy if you already use one of those.)

STEP 2 — Generate the APK
--------------------------------------------------------------
1. Go to https://www.pwabuilder.com
2. Paste your GitHub Pages URL (from Step 1) into the box and click
   "Start".
3. PWABuilder will score your app (it should pass, since manifest +
   service worker + icons are already set up).
4. Click "Package for Stores" -> choose "Android".
5. Keep the default options (it will generate a signing key for you
   automatically — save that key file somewhere safe in case you want
   to update the app later).
6. Download the generated package — you'll get a real, installable
   .apk file.

STEP 3 — Install it on your phone
--------------------------------------------------------------
1. Transfer the .apk to your Android phone (email it to yourself,
   Google Drive, USB, whatever's easiest).
2. Tap the file. Android will ask to allow installing from this
   source the first time — allow it.
3. Install. You now have a real "Battle Plan" app icon on your home
   screen that opens full-screen like any other app.

EDITING YOUR SCHEDULE
--------------------------------------------------------------
Tap "Edit schedule" inside the app any time — add, remove, or change
any block's time, name, or category for weekday or weekend. Changes
save automatically on this device. No need to rebuild the APK for
schedule changes — only rebuild if you want to change the app's
visual design or features.

NOTE ON NOTIFICATIONS
--------------------------------------------------------------
Even as an installed app, Android can suspend background timers for
web apps after a while — this is a platform limit, not a bug. For
guaranteed wake-ups (exercise, automation start, trading open,
trading cutoff, sleep), keep using your phone's native alarms as the
real backstop — those were already set for you separately and don't
depend on this app being open.
