# 📱 Bulk STK Push Bot

Send M-Pesa STK Push requests to multiple phone numbers using the NestLink API.

## Features

- ✅ Paste numbers (one per line or comma-separated)
- ✅ Auto-formats `07XXXXXXXX` → `2547XXXXXXXX`
- ✅ Real-time progress tracking
- ✅ Download results as CSV
- ✅ Rate limiting with configurable delays
- ✅ Beautiful dark UI

## Quick Start (Local)

Simply open `index.html` in your browser. No server needed — it's a pure client-side app.

## Deploy to Render

### Step 1: Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/bulk-stk-push.git
git push -u origin main
```

### Step 2: Deploy on Render

1. Go to [render.com](https://render.com) → **New +** → **Static Site**
2. Connect your GitHub repo
3. Set:
   - **Build Command:** (leave empty)
   - **Publish Directory:** `.` (root)
4. Click **Create Static Site**

Your app will be live at `https://bulk-stk-push.onrender.com`

## Usage

1. Enter your **NestLink API Secret**
2. Set **Amount** and **Description**
3. Paste phone numbers:
   ```
   254712345678
   254723456789
   254734567890
   ```
4. Click **Start Bulk Push**

## API Reference

- **Endpoint:** `https://api.nestlink.co.ke/runPrompt`
- **Method:** POST
- **Headers:** `Api-Secret: your_key`
- **Body:** `{ phone, amount, local_id, transaction_desc }`

## Security Notes

- API key is entered client-side (stored in memory only, not persisted)
- For production, consider adding a backend proxy to hide your API key
