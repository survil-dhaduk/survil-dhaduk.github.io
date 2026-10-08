# ScanPro Developer Website & app-ads.txt Hosting Guide

This folder (`app_website/`) contains the complete developer website for **ScanPro**, including:
- **`app-ads.txt`**: AdMob publisher verification file (`google.com, pub-8840484568079934, DIRECT, f08c47fec0942fa0`).
- **`index.html`**: Clean, modern developer landing page.
- **`privacy-policy.html`**: Store-compliant privacy policy for Google Play Console & Apple App Store.

---

## 🚀 Free Hosting Options (100% Free Forever with HTTPS)

Choose whichever option is easiest for you:

### Option 1: Netlify Drop (Easiest — Takes 60 Seconds, No Git Needed)
1. Go to [https://app.netlify.com/drop](https://app.netlify.com/drop) (log in or create a free account).
2. Drag and drop the **`app_website`** folder directly into the browser upload box.
3. Netlify will deploy it immediately and give you a free live URL (e.g. `https://scanpro-developer.netlify.app`).
4. (Optional) Go to **Site settings → Change site name** to pick a custom free subdomain like `scanpro-app.netlify.app`.
5. Test your file in the browser:
   `https://<your-subdomain>.netlify.app/app-ads.txt`

---

### Option 2: GitHub Pages (Recommended if you use GitHub)
1. Create a new public repository on GitHub (e.g. `scanpro-site` or `<your-username>.github.io`).
2. Upload the contents of `app_website/` to the repository root:
   ```bash
   cd app_website
   git init
   git add .
   git commit -m "Add website, privacy policy, and app-ads.txt"
   git branch -M main
   git remote add origin https://github.com/<your-username>/scanpro-site.git
   git push -u origin main
   ```
3. In your GitHub repo, go to **Settings → Pages**.
4. Under **Source**, select `Deploy from a branch` → choose `main` branch → `/ (root)` → click **Save**.
5. Your site is live at:
   `https://<your-username>.github.io/scanpro-site/app-ads.txt`

---

### Option 3: Vercel (1-Click or CLI)
1. Install Vercel CLI (or import via GitHub on [vercel.com](https://vercel.com)):
   ```bash
   npx vercel app_website --prod
   ```
2. Your site is instantly live at `https://<project-name>.vercel.app/app-ads.txt`.

---

## 📲 How to Connect to Google Play & AdMob

1. **Add Website to Google Play Console**:
   - Go to **Google Play Console** → Select your app → **Store settings** (or Store presence).
   - In the **Website** field, enter your deployed website URL (e.g., `https://your-domain.netlify.app` or `https://yourdomain.com`).
   - In the **Privacy policy** field, enter: `https://your-domain.netlify.app/privacy-policy.html`.
   - Click **Save**.

2. **Verify in Google AdMob**:
   - Go to [AdMob Console](https://admob.google.com/) → **Apps** → **app-ads.txt**.
   - AdMob crawlers check the website listed on your Google Play Store listing daily.
   - Within 24 hours, the status will turn **Green ("Authorized")**!
