# 🎰 PRESENCE Prizes Roulette

A self-contained prize spinner web app built for **Team PRESENCE** at the Aringay National High School STEM Capstone Expo. Players scan a QR code, spin the roulette, and instantly find out what prize they won — complete with a congratulatory message and a preview of exactly what they're taking home.

---

## ✨ Features

- **Slot machine spinner** with animated lights, easing roll, and winner reveal
- **Two prizes with weighted odds** — Keychain + Stickers (25%) and Stickers only (75%)
- **Rich winner card** — random team portrait, prize name, congratulatory message, quote, and images of what they're getting
- **Keychain winner** sees both sides of the acrylic keychain (Side A & Side B preview)
- **Special PRESENCE quote** displayed for each prize type
- **1 spin per device** — powered by `localStorage`; prevents abuse without needing a server
- **QR code generator** built in — always points to the live URL, downloadable as PNG
- **Hidden admin panel** — no visible settings button; only the team knows the secret
- **All assets embedded** — background, portraits, logo, sticker images, keychain previews are all baked into the single HTML file. No internet required after loading.

---

## 🚀 How to Deploy (GitHub Pages — Free)

1. **Rename** the file to `index.html`
2. Go to [github.com](https://github.com) and create a **new public repository** (e.g. `presence-roulette`)
3. Click **Add file → Upload files** and upload `index.html`
4. Go to **Settings → Pages → Branch: main → Save**
5. Wait ~1 minute — your site will be live at:
   ```
   https://yourusername.github.io/presence-roulette/
   ```
6. Open the page, tap the logo **7 times** to open Settings, go to **QR Code**, and download your QR

> **If the site doesn't update after editing:** hard refresh with `Ctrl + Shift + R` (Windows) or `Cmd + Shift + R` (Mac), or open in an incognito window. GitHub Pages can take 1–2 minutes to rebuild.

---

## 🔐 Secret Admin Access

The settings panel has **no visible button**. To open it:

> **Tap or click the PRESENCE logo (the P with the eye) 7 times quickly**

Small red dots appear below the logo as you tap, counting your progress. Stop tapping for 2 seconds and the count resets. Players will never notice.

**Memory trick:** PRESENCE has 8 letters — tap 7 times (one less).

---

## ⚙️ Settings Panel Guide

| Section | What it does |
|---|---|
| **Logo** | Upload a replacement logo — shown on the main page and winner card |
| **Prizes & Odds** | Add, remove, rename prizes and set each one's percentage with a slider. Must total exactly 100% before applying. Use "Even Split" to auto-distribute evenly. |
| **QR Code** | Shows the QR for your live URL. Download it as a PNG to print or display. |
| **Admin Tools** | Reset the spin lock on the current device — useful for testing before the event. |

---

## 🎁 Prize Logic

| Prize | Chance | What the winner gets |
|---|---|---|
| 🔗 Keychain + Stickers | 25% | Acrylic double-sided keychain + PRESENCE logo sticker + Team PRESENCE sticker |
| 🏷 Stickers | 75% | PRESENCE logo sticker + Team PRESENCE sticker |

> Keychain winners also receive both stickers as a bonus on top.

### Special Quotes
- **Keychain:** *"Your presence is the most precious gift you can give to another human being."*
- **Stickers:** *"Be present. Be seen. Be PRESENCE."*

---

## 🔒 One Spin Per Device

Once a player spins, the result is saved to their browser's `localStorage`. If they return to the page, they see a locked screen showing their prize — the spin button is gone.

**Limitations to be aware of:**
- Opening the site in **incognito / private browsing** bypasses the lock (private windows don't persist localStorage)
- Clearing browser data also resets it
- For a casual school event, this is more than sufficient to prevent repeat spinning

**To reset a device for testing:** open Settings (7 taps on logo) → Admin Tools → *Reset Spin Lock (This Device Only)*

---

## 📁 File Structure

```
index.html        ← The entire app. One file, no dependencies, no server needed.
README.md         ← This file.
```

Everything — background image, portraits, logo, sticker previews, keychain images — is base64-encoded and embedded directly in `index.html`. The only external requests are Google Fonts and the QR code library (both loaded from CDN on first visit).

---

## 🛠 Built With

- Vanilla HTML, CSS, JavaScript — no frameworks
- [QRCode Generator](https://github.com/kazuhikoarase/qrcode-generator) (via cdnjs)
- Google Fonts — Abril Fatface, DM Sans, Space Mono
- Browser `localStorage` for spin locking

---

## 👥 Team PRESENCE

**Aringay National High School — STEM Senior High**
Capstone Expo · Einstein 24–25 × Newton 25–26

*"Your presence is the most precious gift you can give to another human being."*
