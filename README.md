# Daily DSA Portal
React + Firebase minimal portal for daily DSA challenges with streaks & leaderboard.


## Features
- Email / Google authentication
- Per-user profile with streak and totalSolved
- Daily challenge (admin can set via Admin page)
- Mark as Completed (atomic transaction per-day)
- Leaderboard sorted by `totalSolved` (ties by streak)
- Admin page to set daily challenge
- Profile edit (name + avatar)
- Optional: FCM push reminders via Firebase Functions
- Optional: Telegram-bot notifier script


---


## Quick setup
1. Clone this repo.
2. `npm install`
3. Create a Firebase project and enable Auth (Email+Google), Firestore, and Cloud Messaging if using notifications.
4. Copy your Firebase config into `src/firebase.js`.
5. (If using Tailwind) `npm run dev` will start the Vite app.


---


## Deploy
- Frontend: Vercel (connect GitHub repo, set env vars)
- Backend (optional): Firebase Functions for scheduled daily notifications and FCM.


Environment variables to set on Vercel / locally:
- VITE_FIREBASE_API_KEY
- VITE_FIREBASE_AUTH_DOMAIN
- VITE_FIREBASE_PROJECT_ID
- VITE_FIREBASE_STORAGE_BUCKET
- VITE_FIREBASE_MESSAGING_SENDER_ID
- VITE_FIREBASE_APP_ID
- TELEGRAM_BOT_TOKEN (if using Telegram)
- TELEGRAM_CHAT_ID (if sending to one group/channel)
