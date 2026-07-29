# SNA Air Service Profile

A live, interactive monthly air service report for John Wayne Airport (SNA), built for Visit Anaheim. Single self-contained `index.html` — no build step, no server-side code, no environment variables needed.

## Deploy this to GitHub + Vercel

You'll need your own GitHub and Vercel accounts for this part — I can't authenticate as you from here, but everything is prepped so this should take about five minutes.

### 1. Create the GitHub repo

1. Go to [github.com/new](https://github.com/new).
2. Name it something like `sna-air-service-profile`.
3. Set visibility to **Public** (as requested).
4. Don't initialize with a README, .gitignore, or license — leave it empty.
5. Click **Create repository** and copy the repo URL it gives you (looks like `https://github.com/<your-username>/sna-air-service-profile.git`).

### 2. Push this folder to it

Open a terminal, `cd` into this folder (the one this README is in), then run:

```bash
git init
git add .
git commit -m "SNA Air Service Profile"
git branch -M main
git remote add origin https://github.com/<your-username>/sna-air-service-profile.git
git push -u origin main
```

(Replace the URL with the one GitHub gave you. If this is your first time pushing from this machine, GitHub will prompt you to log in.)

### 3. Deploy to Vercel

1. Go to [vercel.com/new](https://vercel.com/new) and log in (or sign up — it's free for this).
2. Click **Import Project**, choose **Import Git Repository**, and select the `sna-air-service-profile` repo you just pushed.
3. Vercel will auto-detect it as a static site — no framework, no build command, no environment variables needed. Just click **Deploy**.
4. In under a minute you'll get a live URL like `sna-air-service-profile.vercel.app` that you can share with the SNA research team.

From then on, any time you push a new commit to `main` on GitHub, Vercel automatically redeploys — so future monthly updates are just a `git add . && git commit && git push` away.

## Notes

- This is a static, self-contained HTML file — all CSS and JavaScript are inline, with only Chart.js and Grid.js loaded from a CDN. No API keys or backend required.
- The "Export to PDF" button in the header works the same way once deployed — it just triggers the browser's print dialog with a print-optimized stylesheet.
- If you'd rather keep this private instead of public, you can flip the repo visibility in GitHub's settings at any time — Vercel deployments work the same either way.
