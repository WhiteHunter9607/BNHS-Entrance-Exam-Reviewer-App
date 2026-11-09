# BNHS Entrance Exam Reviewer
- `www/` – the web app (single HTML file + PWA files). Edit `www/index.html` here.
- Web/iOS: deployed to GitHub Pages by `.github/workflows/pages.yml`
- Android: APK built by `.github/workflows/build-apk.yml` (Actions tab → latest run → Artifacts)
When you change the app, bump `CACHE` in `www/sw.js` so installed copies update.
