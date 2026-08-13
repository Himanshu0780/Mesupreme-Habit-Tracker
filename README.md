# Mesupreme™ Habit Tracker

> **It's not over until I win.**

A modern, futuristic habit-tracking Progressive Web App designed to help users build consistent routines, maintain streaks, analyze progress, and receive AI-powered coaching.

Mesupreme combines habit tracking, analytics, focus tools, achievements, screen-time logging, and an optional Claude-powered AI Coach into a single browser-based application.

---

## ✨ Features

### 📋 Habit Tracker

Track daily habits using a monthly grid.

- Monthly habit calendar
- Daily completion tracking
- Habit completion percentages
- Monthly goals
- Current streak calculation
- Habit performance indicators
- Visual progress bars
- Daily completion overview

The application currently includes example habits such as:

- 🌅 Wake up 5AM
- 💧 Drink 3L water
- 💪 Exercise
- 📚 Read 30 mins
- 🧘 Meditate
- 📵 No Social Media
- 🚿 Cold Shower
- ✍️ Journaling
- 🥗 Healthy Eating
- 😴 Sleep 8 Hours

---

### 📊 Analytics

Understand your consistency and progress through visual analytics.

Includes:

- Overall completion percentage
- Habit-specific progress
- Progress rings
- Charts
- Monthly performance
- Streak analysis
- Habit comparisons
- Progress heatmaps

The application uses a charting library bundled into the production build.

---

### 🎯 Focus Mode

Focus Mode provides a simplified view of today's habits.

Instead of navigating through the complete monthly tracker, users can focus on completing today's tasks.

Designed for quick interaction and minimal distractions.

---

### 📱 Screen Time

Track daily screen-time blocks directly inside the application.

This allows users to keep their digital habits alongside their physical and productivity habits.

---

### 🏆 Win Log & Achievements

Mesupreme includes an achievement system designed to reward consistency.

Example achievements include:

- 🌱 First Step
- 💎 Perfect Day
- ⚔️ Week Warrior
- 🔥 Fortnight Fire
- 🌗 Halfway There
- 🌕 Almost There
- 🎖️ Centurion
- 🧩 Habit Master
- 🏗️ Architect
- 👑 Triple Perfect

Achievements are unlocked based on habit activity and progress.

---

### 🤖 AI Coach

Mesupreme includes an optional AI Coach.

The AI Coach can provide:

- Full habit analysis
- Quick actionable tips
- Weekly action plans
- Pattern identification
- Strength analysis
- Areas requiring improvement
- Personalized motivation

The AI Coach supports three coaching styles:

```text
ANALYTICAL
MOTIVATIONAL
STRICT
```

The coaching system receives the user's habit statistics and generates a structured report containing:

```text
💪 STRENGTHS
⚠️ FOCUS AREAS
🔍 KEY PATTERN
🎯 ACTION PLAN
⚡ MOTIVATION
```

---

## 🎉 Perfect Day Celebration

When all configured habits are completed for a day, Mesupreme provides a visual celebration with:

- Confetti animation
- Mission Complete message
- Completion feedback

---

## ⌘ Command Palette

Mesupreme includes a command palette for quick navigation and actions.

Keyboard shortcuts are also supported:

```text
Alt + 1
Alt + 2
Alt + 3
Alt + 4
Alt + 5
Alt + 6
```

The command palette can be opened using:

```text
⌘K
```

or the equivalent keyboard interaction supported by the application.

---

# 🎨 Design

Mesupreme uses a futuristic dark interface inspired by:

- Cyberpunk dashboards
- Command-center interfaces
- Productivity systems
- Gaming HUDs
- Data visualization dashboards

### Design characteristics

- Dark background
- Cyan highlights
- Neon accent colors
- Monospace data typography
- Progress rings
- Animated interactions
- Compact dashboard cards
- Responsive layouts
- Mobile-friendly interactions

Primary visual colors include:

```text
Background: #03060d
Card:       #080f1e
Card 2:     #0b1525
Cyan:       #00e5ff
Amber:      #ffab00
Green:      #00e676
Red:        #ff1744
Purple:     #d500f9
Text:       #c8dae8
Muted:      #4a6070
```

---

# 🧱 Technology Stack

## Frontend

- HTML5
- CSS3
- JavaScript
- React
- React JSX Runtime

## UI / Icons

- Lucide React

## Charts

- Recharts

## Storage

- Browser `localStorage`

## AI

- Anthropic Claude API

## PWA

- Web App Manifest
- Service Worker
- Browser Cache API

## Deployment

Compatible with static hosting platforms such as:

- Vercel
- Netlify
- GitHub Pages
- Other static web hosting platforms

---

# 📁 Project Structure

```text
mesupreme-habit-tracker/
│
├── index.html
├── manifest.json
├── sw.js
├── icon.svg
├── README.md
├── .gitignore
│
└── assets/
    ├── index-CNbz27_W.js
    ├── charts-BgFqocSF.js
    └── index-oXhkbHPF.css
```

---

# 🔍 How the Application Works

Mesupreme is distributed as a production-ready static web application.

The entry point is:

```text
index.html
```

The HTML document loads the compiled JavaScript and CSS files from the `assets` directory.

The application then mounts the React interface into:

```html
<div id="root"></div>
```

The production JavaScript bundle contains the application logic and UI.

---

# 💾 Data Storage

Mesupreme currently uses browser `localStorage`.

There is no database or user account system in the current version.

Habit information and progress are stored locally in the user's browser.

### Important

Clearing browser storage can remove locally stored application data.

Changing browsers or devices will not automatically transfer the data.

---

# 🔐 Privacy

The normal habit-tracking data is stored locally in the browser.

The current application does not require:

- User registration
- Login
- Password
- Database account
- Backend server

This makes the basic habit tracker usable without creating an account.

---

# 🤖 AI Coach Setup

The AI Coach requires an Anthropic API key.

### Step 1

Create an Anthropic API key from your Anthropic account.

### Step 2

Open Mesupreme.

### Step 3

Go to:

```text
AI Coach
```

### Step 4

Enter your API key in the:

```text
API KEY
```

field.

### Step 5

Use the AI Coach to analyze your habit data.

---

## ⚠️ AI API Key Security

**Never commit an API key to GitHub.**

Do not put your API key directly into:

```text
index.html
```

or:

```text
assets/index-CNbz27_W.js
```

Do not put it inside:

```text
README.md
```

Do not upload a file containing your API key.

The current implementation allows users to enter their own key through the application.

### Production consideration

The current AI Coach makes the Anthropic API request directly from the browser.

This is suitable for a personal/demo application where users provide their own API key.

For a public production application serving many users, consider a backend or serverless API layer so API credentials can be managed securely.

---

# 🚀 Run Locally

Because this repository contains a production-ready static build, you don't need to install React or run a build process to test it.

## Option 1: Using `npx serve`

```bash
npx serve .
```

Then open:

```text
http://localhost:3000
```

---

## Option 2: VS Code Live Server

1. Open the project folder.
2. Install the Live Server extension.
3. Right-click `index.html`.
4. Select **Open with Live Server**.

---

## Option 3: Directly Open `index.html`

You can double-click `index.html`.

However, this is not recommended for testing all features because some browser functionality, especially service workers and module loading, works more reliably through HTTP/HTTPS.

---

# 📱 Progressive Web App

Mesupreme includes PWA functionality.

The project contains:

```text
manifest.json
sw.js
```

The manifest defines:

- Application name
- Short name
- Theme color
- Background color
- Display mode
- Orientation
- Application icon
- Application shortcuts

The application can be installed from supported browsers.

---

## Install on Desktop Chrome

1. Open the deployed Mesupreme website.
2. Look for the install icon in the browser address bar.
3. Select **Install**.

---

## Install on Android

1. Open the website in Chrome.
2. Open the browser menu.
3. Select **Add to Home screen** or **Install app**.

---

## Install on iPhone

Open the application in Safari:

```text
Share → Add to Home Screen
```

---

# ⚡ Service Worker

The project includes a service worker:

```text
sw.js
```

The service worker provides browser caching functionality and allows the application to behave more like an installable web application.

The current cache version is:

```text
mesupreme-v1
```

When deploying a significantly updated version, consider updating the cache version.

For example:

```javascript
const CACHE = 'mesupreme-v2';
```

---

# ☁️ Deploy to Vercel

Vercel is recommended for hosting this project.

## Step 1: Create a GitHub repository

Create a new repository:

```text
mesupreme-habit-tracker
```

Make sure `index.html` and `assets/` are in the repository root.

Correct:

```text
repository/
├── index.html
├── manifest.json
├── sw.js
├── icon.svg
└── assets/
```

Incorrect:

```text
repository/
└── mesupreme-github-ready/
    ├── index.html
    └── assets/
```

---

## Step 2: Connect GitHub to Vercel

In Vercel:

```text
Add New Project
→ Import Git Repository
→ Select mesupreme-habit-tracker
```

---

## Step 3: Configure the project

Because this is already a production build:

```text
Framework Preset: Other
Build Command: None
Output Directory: .
Install Command: None
```

Then deploy.

---

# 🌐 Deployment to Netlify

Mesupreme can also be deployed using Netlify.

You can:

1. Connect the GitHub repository.
2. Or upload the static project directly.

The project root should contain:

```text
index.html
assets/
manifest.json
sw.js
icon.svg
```

---

# 🐙 GitHub Setup

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/mesupreme-habit-tracker.git
```

Move into the project:

```bash
cd mesupreme-habit-tracker
```

Check the files:

```bash
git status
```

Add the files:

```bash
git add .
```

Create the first commit:

```bash
git commit -m "Initial release of Mesupreme Habit Tracker"
```

Push:

```bash
git push origin main
```

---

# 🔄 Updating the Project

Whenever you make changes:

```bash
git status
git add .
git commit -m "Update habit tracker"
git push
```

If Vercel is connected to GitHub, new commits can automatically trigger a deployment.

---

# 🧪 Testing Checklist

Before publishing a new version, check:

- [ ] Application loads correctly
- [ ] Dashboard loads
- [ ] Habit grid works
- [ ] Habit completion works
- [ ] Streaks update correctly
- [ ] Analytics load
- [ ] Charts display correctly
- [ ] Focus Mode works
- [ ] Screen Time works
- [ ] Win Log works
- [ ] Achievement badges update
- [ ] AI Coach opens
- [ ] AI Coach handles missing API key
- [ ] AI Coach responds with a valid API key
- [ ] Command palette works
- [ ] Keyboard shortcuts work
- [ ] Mobile layout works
- [ ] PWA manifest loads
- [ ] Service worker registers
- [ ] Application can be installed
- [ ] Data survives page refresh

---

# 🛠️ Troubleshooting

## Blank page

Check that the assets are located inside:

```text
assets/
```

and not in the repository root.

The HTML expects:

```text
./assets/index-CNbz27_W.js
./assets/charts-BgFqocSF.js
./assets/index-oXhkbHPF.css
```

---

## Charts aren't loading

Make sure:

```text
charts-BgFqocSF.js
```

exists inside:

```text
assets/
```

Also test the application through a local web server instead of opening `index.html` directly.

---

## AI Coach doesn't respond

Check:

1. An Anthropic API key has been entered.
2. The key is valid.
3. The browser has internet access.
4. The API request is not being blocked.
5. Check the browser console for errors.

---

## Data disappeared

The application stores data locally in the browser.

Data can be lost if:

- Browser storage is cleared.
- Site data is deleted.
- A different browser/device is used.
- Private/incognito browsing is used.

The current version does not synchronize data between devices.

---

# 📈 Future Improvements

Potential improvements include:

- User authentication
- Cloud database
- Cross-device synchronization
- Habit creation and editing
- Custom habit categories
- Custom colors and icons
- Habit reminders
- Push notifications
- Data export/import
- CSV export
- JSON backup
- Advanced analytics
- Weekly reports
- Monthly reports
- AI-generated habit recommendations
- Secure backend API for AI requests
- User profiles
- Cloud backup
- Dark/light themes
- Custom dashboard layouts

---

# 🗺️ Roadmap

## Version 1.0

- [x] Habit tracking
- [x] Monthly habit grid
- [x] Streak tracking
- [x] Analytics
- [x] Focus Mode
- [x] Screen Time
- [x] Win Log
- [x] Achievement system
- [x] AI Coach
- [x] Command palette
- [x] Keyboard shortcuts
- [x] PWA support
- [x] Local storage

## Version 2.0

- [ ] User accounts
- [ ] Cloud synchronization
- [ ] Habit editor
- [ ] Habit reminders
- [ ] Push notifications
- [ ] Data import/export
- [ ] Secure AI backend
- [ ] Advanced AI insights
- [ ] Multi-device synchronization

---

# 📄 License

This project is intended as a personal/portfolio project.

If you plan to distribute the application publicly or commercially, add an appropriate open-source or proprietary license.

---

# 👨‍💻 Author

**Himanshu**

Computer Science & Engineering Student

---

# ⭐ Project

If you find Mesupreme useful, consider giving the repository a ⭐ on GitHub.

> **It's not over until I win.**
