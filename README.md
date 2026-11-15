# 2027 Planner: website and phone app

This folder is the complete website. It has no build step, no server code and no accounts. Upload the whole folder as it is.

```
index.html             the planner (all pages, styles and code in one file)
manifest.webmanifest   app name, icons and colours used when it is added to a home screen
sw.js                  makes the planner open and work offline
icons/                 app icons (home screen, browser tab)
fonts/                 IBM Plex fonts, stored here so nothing loads from other websites
.nojekyll              tells GitHub Pages to publish the files as they are
README.md              these instructions
```

## Where your data lives

- Everything you type is stored **on the device you are using**, inside that browser or home-screen app. It is never sent to the website host or anyone else.
- Publishing the site makes the **empty app** public. Anyone with the link gets their own blank planner. They can't see your entries.
- Your phone and your computer keep **separate copies**. They do not sync. Use **Settings > Data > Export backup** on one device and **Import backup file** on the other to move your data.
- **On iPhone, the home-screen app and the Safari website keep separate data.** Add the planner to your home screen first, then only use it from the icon.
- Deleting the home-screen app, or clearing the site's data in browser settings, deletes the entries. **Export a backup once a month.**

## Step 1: Put the website online (pick one)

The site must be served over **HTTPS** for offline use and home-screen install. Both options below do that for free.

### Option A: Netlify (easiest, about 5 minutes)

1. Go to **app.netlify.com/signup** and create a free account (email, GitHub or Google). Sign up *before* uploading: Netlify deletes sites uploaded without an account after about an hour.
2. Go to **app.netlify.com/drop**.
3. Unzip `planner-2027-website.zip` on your computer, then drag the **folder** (the one containing `index.html`) onto the page.
4. When it finishes, you get a link like `https://random-name-123.netlify.app`. Open it to check.
5. Optional: in the project, open **Project configuration > Change project name** to get a nicer address, such as `https://elyzer-planner-2027.netlify.app`.

**To update the site later:** open the project in Netlify, go to **Deploys**, and drag the new folder onto the drop area. Your data on your devices is not affected.

### Option B: GitHub Pages

1. Sign in at **github.com** and create a new **public** repository, for example `planner-2027`.
2. On the repository page choose **Add file > Upload files**. Drag in **everything inside** the unzipped folder (so `index.html` sits at the top level, not inside a subfolder). Include the `icons` and `fonts` folders. Click **Commit changes**.
3. Open **Settings > Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**, **Branch** to `main` and folder `/ (root)`. Click **Save**.
4. Wait 1 to 2 minutes. The address appears at the top of that page, for example `https://your-username.github.io/planner-2027/`.

**To update later:** upload the changed files again with **Add file > Upload files** and commit.

## Step 2: Add it to your phone's home screen

Open your site's link on the phone first.

### iPhone or iPad

1. Open the link in **Safari**.
2. Tap the **Share** button (the square with an up arrow). On recent iOS versions it may be under the **...** button.
3. Scroll down and tap **Add to Home Screen**.
4. Keep the name "Planner 2027" and tap **Add**.
5. Open the planner from the new icon. It opens full screen without the Safari address bar.

Chrome and Edge on iPhone also offer **Add to Home Screen** from their Share menu.

### Android

1. Open the link in **Chrome**.
2. Tap **Install** if a prompt appears at the bottom. Otherwise tap the **⋮** menu, then **Add to home screen** (or **Install app**), then **Install**.
3. The planner appears on your home screen and in your app drawer. Long-press the icon for shortcuts to Today, Tasks and Habits.

On a computer, Chrome and Edge show an install icon in the address bar, and **Settings** in the planner has an **Install the planner** button when the browser allows it.

## Step 3: Check it

- The chip at the bottom of the menu should read **Saved on this device**.
- Add a task, close the app fully, and reopen it. The task should still be there.
- Turn on airplane mode and open the app. It should still open with your data.

## If you already used the planner inside Claude

Open that version, go to **Settings > Data > Export backup (JSON)**, move the file to the device you'll use, then in the new app choose **Settings > Data > Import backup file**.

## Troubleshooting

- **"Add to Home Screen" is missing on iPhone:** make sure you are in Safari (or Chrome/Edge on iOS 16.4 or later), not inside another app's built-in browser such as Messenger or Facebook. Use "Open in Safari" first.
- **No Install option on Android:** check that the address starts with `https://`. Wait a few seconds after the page loads, then try the menu again.
- **An update doesn't show:** close the app completely and reopen it twice. The first open downloads the update; the next one uses it.
- **The site shows a 404 on GitHub Pages:** `index.html` must be at the top level of the repository, and Pages must be set to the `main` branch, `/ (root)`.

## Licences

IBM Plex fonts: SIL Open Font License 1.1 (see `fonts/LICENSE.txt`).
