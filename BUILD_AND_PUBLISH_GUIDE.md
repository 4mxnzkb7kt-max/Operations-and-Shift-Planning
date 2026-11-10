# 24/7 Shift Planner: Deployment & App Store Publishing Guide

## 1. Direct Web / PWA Deployment (Ready in 2 Minutes)
This package is already a production-ready Progressive Web App (PWA).

### Option A: Free 1-Click Hosting via Vercel or Netlify
1. Go to [vercel.com](https://vercel.com) or [netlify.com](https://netlify.com).
2. Drag and drop this folder (`shift_planner_package`) directly into the dashboard.
3. You will get a live secure URL (e.g., `https://your-shift-planner.vercel.app`).
4. Anyone opening this link on Android or desktop will see an **"Install App"** prompt, adding it directly to their home screen as a standalone app!

### Option B: Free Hosting via GitHub Pages
1. Push this folder to a GitHub repository.
2. In Repository Settings -> Pages, select `main` branch -> save.
3. Your app is live at `https://<username>.github.io/<repo>/`.

---

## 2. Generating Android APK for Amazon Appstore & Samsung Galaxy Store

Amazon Appstore and Samsung Galaxy Store accept standard `.apk` or `.aab` files.

### Step 1: Install Capacitor CLI (1 command)
In a folder with your `index.html` and `manifest.json`:
```bash
npm init -y
npm install @capacitor/core @capacitor/cli @capacitor/android
npx cap init "Shift Planner" "com.shiftplanner.app" --web-dir "."
npx cap add android
npx cap open android
```

### Step 2: Build APK in Android Studio
1. Android Studio will open automatically.
2. Go to **Build -> Build Bundle(s) / APK(s) -> Build APK(s)** (or **Generate Signed Bundle / APK** for release).
3. The resulting `.apk` file is ready to upload to both Amazon and Samsung!

---

## 3. Submitting to Amazon Appstore (Zero Testing Mandate)
1. Sign up for a free developer account at [developer.amazon.com](https://developer.amazon.com).
2. Click **Add a New App -> Android**.
3. Upload your `.apk` generated above.
4. Set your price (Free or Paid, e.g. $4.99).
5. Add your title, description, and screenshots.
6. Submit for review (typically approved in 24-48 hours).

---

## 4. Submitting to Samsung Galaxy Store (Zero Testing Mandate)
1. Register at the [Samsung Developer Console](https://developer.samsung.com/galaxy-store).
2. Click **Add New Application -> Android**.
3. Upload the same signed `.apk`.
4. Fill in the store listing information and screenshots.
5. Choose your pricing and target countries.
6. Click **Submit** for Samsung's QA review.
