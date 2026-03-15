# 🏛️ CivicEase — Smart Living for Every Citizen

A smart life management app for Jamaican public sector workers and low-to-middle-income households. Manage bills, track your budget, plan meals, monitor medications, and navigate your daily commute — all powered by AI.

-----

## 📁 Project Structure

```
civicease/
├── CivicEase_TealGold.html   ← The full app (open this in a browser)
├── server.js                 ← Backend API proxy (keeps your key safe)
├── package.json              ← Node.js dependencies
├── .gitignore                ← Prevents .env from being uploaded
├── .env.example              ← Template for your environment variables
├── .env                      ← YOUR REAL KEY (never uploaded to GitHub)
└── README.md                 ← This file
```

-----

## 🚀 Deploy in 4 Steps

### Step 1 — Push to GitHub

1. Create a new repository on [github.com](https://github.com) — make it **Public**
1. On your computer, open a terminal in this folder and run:

```bash
git init
git add .
git commit -m "Initial CivicEase commit"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
git push -u origin main
```

> ✅ The `.gitignore` file ensures your `.env` (real API key) is **never uploaded**.

-----

### Step 2 — Create a Free Account on Render

1. Go to [render.com](https://render.com) and sign up (free)
1. Click **“New +”** → select **“Web Service”**
1. Click **“Connect GitHub”** and authorise Render to access your repo
1. Select your **civicease** repository

-----

### Step 3 — Configure the Web Service

Fill in these settings on Render:

|Field            |Value                              |
|-----------------|-----------------------------------|
|**Name**         |`civicease` (or any name you like) |
|**Region**       |US East (Ohio) — closest to Jamaica|
|**Branch**       |`main`                             |
|**Runtime**      |`Node`                             |
|**Build Command**|`npm install`                      |
|**Start Command**|`node server.js`                   |
|**Instance Type**|`Free`                             |

-----

### Step 4 — Add Your API Key on Render

1. Scroll down to the **“Environment Variables”** section
1. Click **“Add Environment Variable”**
1. Set:
- **Key:** `ANTHROPIC_API_KEY`
- **Value:** `sk-ant-your-real-key-here` ← paste your actual key here
1. Click **“Create Web Service”**

Render will build and deploy your server. In about 2 minutes you’ll get a live URL:

```
https://civicease.onrender.com
```

-----

### Step 5 — Host the HTML on GitHub Pages (optional)

To make the app itself publicly accessible without needing to open a file:

1. In your GitHub repo, go to **Settings → Pages**
1. Under **Source**, select **main branch** and click **Save**
1. Your app will be live at:
   
   ```
   https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/CivicEase_TealGold.html
   ```

Share that link with anyone — they open it, complete the setup wizard, and CivicEase works fully with no API key needed from them.

-----

## 🔑 Getting Your Anthropic API Key

1. Go to [console.anthropic.com](https://console.anthropic.com)
1. Sign up for a free account
1. Go to **Settings → API Keys**
1. Click **“Create Key”**
1. Copy the key — it starts with `sk-ant-`
1. Paste it into Render’s Environment Variables (Step 4 above)

> New accounts get free credits to get started. After that, usage is pay-as-you-go.
> Casual use of CivicEase costs approximately **$0.003 per conversation**.

-----

## ⚠️ Important Security Rules

|Rule                                                 |Why                                     |
|-----------------------------------------------------|----------------------------------------|
|Never paste your API key into the HTML file          |Anyone can view source and steal it     |
|Never commit `.env` to GitHub                        |Bots scan GitHub for exposed keys 24/7  |
|Always add the key via Render’s Environment Variables|It’s encrypted and never visible in code|
|Your `.gitignore` already protects you               |`.env` is blocked from being uploaded   |

-----

## 🛠️ Running Locally (for development)

```bash
# 1. Install dependencies
npm install

# 2. Create your .env file
cp .env.example .env
# Then edit .env and add your real API key

# 3. Start the server
npm start

# Server runs at http://localhost:3000
# Open CivicEase_TealGold.html in your browser
```

-----

## 💰 Cost Estimate

|Users|Daily Messages|Monthly Cost|
|-----|--------------|------------|
|10   |50 total      |~$0.15      |
|50   |200 total     |~$0.60      |
|200  |500 total     |~$1.50      |

Render free tier: $0/month. Anthropic: pay-as-you-go from above.

-----

## 📞 Support

Built with ❤️ for Jamaica. Powered by [Claude by Anthropic](https://anthropic.com).
