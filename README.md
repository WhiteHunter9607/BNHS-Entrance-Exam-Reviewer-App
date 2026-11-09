# BNHS Entrance Exam Reviewer

A mobile-friendly reviewer app for the BNHS entrance exam. It works **offline** once installed.

- **Web app (iPhone / iPad / any browser):** https://whitehunter9607.github.io/BNHS-Entrance-Exam-Reviewer-App/
- **Android APK:** [Download the latest APK](../../releases/tag/apk-latest)

---

## 📱 Install on Android (APK)

1. On your phone, open the **[Releases page](../../releases/tag/apk-latest)**.
2. Under **Assets**, tap **app-debug.apk** to download it.
3. Open the downloaded file (check your **Downloads** folder or the notification).
4. If Android says *"For your security, your phone is not allowed to install unknown apps from this source"*:
   - Tap **Settings**
   - Turn on **Allow from this source**
   - Go back and tap **Install**
5. If Google Play Protect shows a warning, tap **More details → Install anyway**. The app is safe, it just isn't from the Play Store.
6. Tap **Open**. The app now works with no internet.

> To update: download and install the newest APK the same way. Your progress is kept.

---

## 🍎 Install on iPhone / iPad (offline web app)

You **must use Safari**. Other browsers can't add the app to the Home Screen.

1. Open Safari and go to:
   **https://whitehunter9607.github.io/BNHS-Entrance-Exam-Reviewer-App/**
2. **Wait for the page to fully load** while you're online. This saves it for offline use.
3. Tap the **Share** button (the square with an arrow pointing up).
4. Scroll down and tap **Add to Home Screen**.
5. Tap **Add** in the top right.
6. Open the app from the new **BNHS Reviewer** icon on your Home Screen.

**Test offline:** turn on Airplane Mode and open the app. It should still load.

---

## 💻 Use on a computer

Open the web link above in Chrome or Edge. To install it, click the install icon at the right of the address bar.

---

## ❓ Troubleshooting

| Problem | Fix |
|---|---|
| Android won't install the APK | Allow "Install unknown apps" for your browser or file manager, then try again. |
| "App not installed" on Android | Uninstall any older copy first, then install again. |
| iPhone has no "Add to Home Screen" | Open the link in **Safari**, not Chrome or Messenger. |
| App doesn't open offline on iPhone | Open it once online first, and add it from Safari. |
| Not showing the newest version | Close and reopen the app while online. Reloading once also helps. |
| Scores or progress missing | Progress is saved on that device only. Clearing browser data or uninstalling the app erases it. |

---

## 🛠️ For the developer

| Path | What it does |
|---|---|
| `www/index.html` | The whole app. Edit this file. |
| `www/sw.js` | Offline cache. **Change `bnhs-reviewer-v1` to `v2`, `v3`, … on every update** so installed copies refresh. |
| `www/manifest.webmanifest` | Home-screen name, colours and icons. |
| `.github/workflows/pages.yml` | Publishes `www/` to GitHub Pages on every push to `main`. |
| `.github/workflows/build-apk.yml` | Builds the APK (Capacitor) and attaches it to the **apk-latest** release. |

**Update the app:** edit `www/index.html`, bump the cache name in `www/sw.js`, then commit and push to `main`. Both workflows run on their own: the website updates in about a minute, and the APK takes about 5 to 10 minutes.

**Repo settings needed once:**
- Settings → Pages → Source: **GitHub Actions**
- Settings → Actions → General → Workflow permissions: **Read and write permissions**
