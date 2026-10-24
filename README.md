# Recomp Tracker: GitHub setup

You will make **two repos**: a public one that hosts the website, and a private one that stores your data.
The website repo never contains your data, so it is safe to keep public (GitHub Pages is free for public repos).

## 1. Create your GitHub account
Sign up at https://github.com/signup. This is your ID and password.

## 2. Host the website
1. Click **+ → New repository**. Name it `recomp-tracker`, keep it **Public**, then **Create repository**.
2. Click **uploading an existing file**, drag in `index.html`, then **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment*, choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. After a minute your site is live at `https://YOUR-USERNAME.github.io/recomp-tracker/`. Bookmark it, or use "Add to Home Screen" on your phone.

## 3. Create the private data repo
1. **+ → New repository**. Name it `recomp-data`, set it to **Private**, and tick **Add a README file**. Create it.

## 4. Create an access token
1. Profile picture → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Name: `recomp-tracker`. Choose an expiration (the maximum is 1 year).
3. *Repository access* → **Only select repositories** → pick `recomp-data`.
4. *Permissions → Repository permissions → Contents* → **Read and write**.
5. **Generate token** and copy it right away. GitHub only shows it once.

## 5. Connect each device
1. Open your site → **Data** tab → **Cloud sync**.
2. Enter `YOUR-USERNAME/recomp-data` and paste the token → **Connect**.
3. Repeat on every phone or computer you use. Your data syncs automatically after that.

## Moving your existing data
If you already have data in the Claude-hosted version, open its **Data** tab, download the `.json` backup, then import it on the new site **before** you connect sync.

## Good to know
- The token is saved in that browser only. Don't connect on a shared or public device. You can revoke it any time in GitHub's token settings.
- When the token expires, make a new one and tap **Disconnect**, then connect again. Your data stays in the repo.
- If two devices change data before syncing, the page asks you which copy to keep, so nothing is overwritten silently.
- The latest data lives in `data.json` in your private repo. Its commit history is an automatic backup.
