# Расписание служений — Church Schedule App

A shared church service scheduling app with real-time sync via Firebase.

## Quick Setup (10 minutes)

### Step 1: Create Firebase Project (free)

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Click **"Create a project"** → name it `church-schedule` → Create
3. Go to **Build → Realtime Database** → **Create Database**
4. Choose any location → Select **"Start in test mode"** → Enable
5. Go to **Project Settings** (⚙️ gear icon) → scroll to **"Your apps"** → click web icon **`</>`**
6. Nickname: `church-schedule` → **Register app**
7. Copy the `firebaseConfig` object — you'll need it in Step 2

### Step 2: Add your Firebase config

Open `index.html` and find this block near the top (around line 30):

```js
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  ...
};
```

Replace it with your config from Step 1.

### Step 3: Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g. `church-schedule`)
2. Push this folder to the repo:

```bash
git init
git add .
git commit -m "Church schedule app"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/church-schedule.git
git push -u origin main
```

3. Go to your repo on GitHub → **Settings** → **Pages**
4. Under "Source" select **Deploy from a branch**
5. Branch: **main**, folder: **/ (root)** → **Save**
6. Wait 1-2 minutes — your site will be live at:
   `https://YOUR_USERNAME.github.io/church-schedule/`

### Done!

Share the URL with your church team. Everyone sees the same schedule with real-time sync.

## Features

- 📅 Monthly schedule with Sunday AM/PM and Thursday services
- 👥 Volunteer management with role assignments
- 🔄 Real-time sync — changes appear instantly for all users
- ⚡ Auto-populate with smart assignment rules
- 🖨️ Print view for clean printable output
- 📥 JSON export for PDF generation
- 🍷 Communion team management
- 📊 Availability grid

## Security Note

The default Firebase rules allow open read/write access. This is fine for a church team app. If you want to restrict access later, update your Firebase Realtime Database rules.
