# Loop

A personal tracker for open loops. One static page, no server, no account, no build step.

## Put it on GitHub Pages

1. On github.com, create a new repository (for example `loop`). It must be **public** unless you have a paid GitHub plan.
2. Open the repository, choose **Add file → Upload files**, and upload every file in this folder:
   `index.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png`, `README.md`.
   They all sit at the top level; there are no subfolders.
3. Commit the upload.
4. Go to **Settings → Pages**. Under "Build and deployment", set Source to **Deploy from a branch**, Branch to **main** and folder to **/ (root)**. Save.
5. After a minute or two the page is live at `https://YOUR-USERNAME.github.io/loop/`.

## Put it on your phone

Open the address in Safari (iPhone) or Chrome (Android), then use **Share → Add to Home Screen** (Safari) or **⋮ → Add to Home screen / Install app** (Chrome). It then opens full screen and works with no connection.

## Where your data lives

- Your loops are stored in the browser on the device you use, and nowhere else. The public repository holds only the empty app, so nobody who finds it can see your loops.
- Nothing syncs. Your phone and your laptop each keep their own copy.
- To back up or move devices: gear icon → **Export backup**, then **Import backup** on the other device. Importing replaces what is there.
- Clearing the browser's site data for this address erases your loops. Safari can also clear data for sites you have not opened in several weeks unless the app is on your Home Screen. Export a backup regularly.

## How it works

- **Stages:** Simmering, Active, Waiting on, Stuck, Closed. Every change is written to the loop's history.
- **Closing:** Completed, Decided not to, or Superseded. All three are real closures.
- **Next steps:** break a loop into smaller steps; the next unticked one shows on its card.
- **Quiet loops:** a loop untouched for 7 days is flagged on its card and in the greeting.
- **Month:** commit loops to the month, each with a weight of 1 to 3, then lock the set.
  Score = weight of committed loops closed as Completed ÷ weight of all committed loops, leaving out any closed as Decided not to or Superseded.
  The score unlocks the rewards you set at each threshold.
- **Receipts:** every closed loop, how long it was open, and (once three loops have both an estimate and a real time) how far off your estimates run.

## Changing it

Everything is in `index.html`. Edit, upload the new file over the old one, and the live page updates on the next visit with a connection. If you add or rename files, add them to the `CORE` list in `sw.js` and change `loop-v1` to `loop-v2`.
