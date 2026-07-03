# Recovery Tracker

Steve Ridgeway — ACL reconstruction recovery, 20 July 2026.

## Set up in 4 steps

### Step 1 — Create the repo

Go to github.com, click **New repository**, name it `knee-recovery`, set it to Public, click Create.

### Step 2 — Upload the files

In the new repo, click **uploading an existing file** and drag everything in this folder (including the `.github` folder) into the upload box. Commit to main.

### Step 3 — Enable GitHub Pages

Go to **Settings → Pages → Source** and select `main` branch, root folder. Click Save. Wait two minutes, then visit:

```
https://ridgetests.github.io/knee-recovery/
```

### Step 4 — Add to home screen (iPhone)

On your iPhone, open the URL in Safari. Tap the **Share** button (box with arrow) → **Add to Home Screen** → Add. The Recovery icon will appear on your home screen and open full-screen.

---

## Daily nudges (optional but recommended)

The daily nudge arrives via the free **ntfy.sh** service — no account needed.

### a) Pick a topic name

Choose something unique like `ridgeway-recovery-2026` (keep this private).

### b) Subscribe on your phone

Download the **ntfy** app from the App Store. Open it, tap the + button, enter your topic name. Notifications will arrive here every morning.

### c) Add the secret to GitHub

In the repo, go to **Settings → Secrets and variables → Actions → New repository secret**.
- Name: `NTFY_TOPIC`
- Value: your topic name (e.g. `ridgeway-recovery-2026`)

Click Add secret. Done — the GitHub Action will send a nudge every morning at 8am BST.

To test it immediately: go to **Actions → Daily recovery nudge → Run workflow**.

---

## Notes

- All data saves locally to your phone — nothing leaves the device
- Works offline once installed
- The nudge is a generic morning reminder (it can't read your actual data from your phone)
- Winter time: edit `.github/workflows/daily-nudge.yml` and change `0 7` to `0 8` in the cron line
