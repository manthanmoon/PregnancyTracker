# Bloom Pregnancy Tracker (Installable PWA)

## What this is
A mobile-friendly installable web app with:
- Pregnancy week and estimated due-date calculation from LMP
- Baby-development overview text
- Local notes and date settings
- Offline shell caching after the first visit

## Important privacy and medical limitations
This is a starter/demo app. It stores the profile and notes in browser localStorage on the device. It has no cloud sync, real account/login, encryption, backup, or access control. Anyone with access to the same browser profile may be able to view the stored data. Do not store sensitive medical information on a shared device.
Pregnancy weeks and due dates are estimates and should be confirmed by a healthcare professional. The app is not medical advice.

## Quick local preview
Opening `index.html` directly lets you preview the app, but service workers and installability generally require HTTPS or localhost.

## Install on an Android phone
1. Upload the contents of this folder to a static HTTPS host, such as GitHub Pages or Netlify. Keep `index.html`, `manifest.webmanifest`, `sw.js`, and `icons/` together.
2. Open the HTTPS URL in Chrome on Android.
3. Open Chrome's menu (three dots) and tap **Install app** or **Add to Home screen** (the wording depends on Chrome version).
4. Confirm. The app icon will appear on the home screen.

## Test on your computer
For example, if Python 3 is installed, open a terminal in this folder and run:
    python -m http.server 8000
Then visit `http://localhost:8000` in your browser. For Android installability, deploy to HTTPS.

## To make this production-ready
Use a backend authentication provider and database, enforce authorization, store only necessary data, add a privacy policy and consent flow, and avoid handling passwords yourself. Do not use localStorage as secure storage for real medical records.
