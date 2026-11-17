# Khmer Wedding Invitation Website · គេហទំព័រធៀបការឌីជីថល

A luxury digital wedding invitation website featuring an interactive envelope wax-seal opening, Khmer/English bilingual support, countdown timer, event schedule, love story strip, photo gallery lightbox, Google Maps venue direction, and bank QR gift cards.

---

## 🚀 Quick Vercel Deployment Guide

### Option A: Deploy as a standalone repository (Recommended)
1. Initialize git in this folder or upload this folder (`wedding_project_2`) to a new GitHub repository.
2. Go to [vercel.com](https://vercel.com) and click **"Add New..."** -> **"Project"**.
3. Import your GitHub repository.
4. Leave Framework Preset as **"Other"** (static site).
5. Click **"Deploy"**.
6. (Optional) In Project Settings -> Domains, add your custom domain or customize your `*.vercel.app` slug (e.g. `dara-sophea.vercel.app`).

### Option B: Deploy from the parent multi-project repository
1. If deploying the parent repository containing `wedding_project_2`:
2. In Vercel Project Settings -> **General** -> **Root Directory**, set it to `wedding_project_2`.
3. Save and redeploy.

---

## 📁 Project Folder Structure

```
wedding_project_2/
├── index.html                 # Main website template & configuration
├── vercel.json                # Vercel caching, audio streaming & security headers
├── .gitignore                 # Excludes OS files, temp files & backups
├── .vercelignore              # Keeps internal PDFs & generators private
├── guest-links.html           # Offline guest link generator tool
├── handbook/
│   └── Khmer Wedding Invitation Handbook.pdf  # Detailed guide
├── photos/
│   └── README.txt             # Photo placement & dimension guidelines
└── README.md                  # This file
```

---

## 📝 Customizing Wedding Details

Open `index.html` and search for:
```javascript
/* ============ EDIT THIS PART FOR EACH CUSTOMER ============ */
const C = {
  // Groom and Bride details (Khmer & English)
  // Date & times
  // Venue & Google Maps link
  // Telegram RSVP & phone number
  // Bank accounts & QR codes
  // Photos & background music
};
```

### When Ready to Add Photos:
Place JPG photos into the `photos/` folder:
- `hero1.jpg`, `hero2.jpg` — Banner photos
- `couple1.jpg`, `couple2.jpg` — Couple portraits
- `s1.jpg`, `s2.jpg`, `s3.jpg` — Love story photos
- `1.jpg` to `12.jpg` — Photo gallery
- `qr1.jpg`, `qr2.jpg` — Bank QR codes

*Note: Missing photos gracefully show an elegant silhouette, so the site never looks broken before or during uploads.*

### When Ready to Add Background Music:
1. Place your audio file in the project root named `music.mp3` (under 4MB recommended).
2. In `index.html`, set:
   ```javascript
   music: 'music.mp3',
   ```
   Music will start playing smoothly when guests tap the envelope seal.

---

## 💌 Personalized Guest Links

Use `guest-links.html` (open locally in your browser) to batch generate personalized invitation links:

- **Khmer (Default):** `https://your-site.vercel.app/?to=លោក+សុខា`
- **English First:** `https://your-site.vercel.app/?to=Mr.+David&lang=en`

Guests opening their link will see their name honored on the envelope wax seal and invitation card!
