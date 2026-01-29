# Culinary Class Wars - Dinner Party Game

A Culinary Class Wars themed dinner party game with AI-powered judging by Paik Jong Won and Anh Sung Jae.

## 🚀 Quick Deploy to Vercel

### Prerequisites
- GitHub account
- Anthropic API key (get one at https://console.anthropic.com)

### Deployment Steps

1. **Create a GitHub Repository**
   - Go to https://github.com/new
   - Name it something like `culinary-class-wars`
   - Make it public or private
   - Don't initialize with README

2. **Upload Files to GitHub**
   - Upload all files from this folder to your new repository
   - Make sure the structure is:
     ```
     /api/judge.js
     /public/index.html
     /vercel.json
     /package.json
     ```

3. **Deploy to Vercel**
   - Go to https://vercel.com
   - Click "Add New Project"
   - Import your GitHub repository
   - Click "Deploy"
   - Wait 1-2 minutes for deployment to complete

4. **Done! 🎉**
   - Vercel will give you a URL like `https://your-project.vercel.app`
   - Open that URL and use your Anthropic API key when prompted
   - No more CORS issues!

## 📁 File Structure

```
culinary-class-wars-vercel/
├── api/
│   └── judge.js          # Serverless function that proxies to Anthropic API
├── public/
│   └── index.html        # Your game HTML
├── vercel.json           # Vercel configuration
├── package.json          # Node.js project config
└── README.md            # This file
```

## 🔧 Local Development (Optional)

If you want to test locally:

1. Install Vercel CLI:
   ```bash
   npm install -g vercel
   ```

2. Run locally:
   ```bash
   cd culinary-class-wars-vercel
   vercel dev
   ```

3. Open http://localhost:3000

## 💡 How It Works

- The HTML frontend runs in the browser
- When judging, it calls `/api/judge` (your Vercel serverless function)
- The serverless function forwards the request to Anthropic's API
- This bypasses CORS restrictions since the API call happens server-side

## 🎮 How to Use

1. Set number of contestants and bad ingredients
2. Assign ingredients randomly
3. Each contestant submits their dish (name can be customized)
4. Enter your Anthropic API key
5. Click "Judge All Dishes" for instant feedback from both judges
6. Michelle gets special birthday treatment! 🎂

## 📝 Notes

- Your API key is sent directly to the serverless function (not stored anywhere)
- Each judgment costs ~$0.01-0.03 from your Anthropic account
- The serverless function is free on Vercel (up to 100GB bandwidth/month)

## 🎉 Features

- Random ingredient assignment (1 protein + 1 non-protein + optional bad ingredient)
- Editable contestant names for personalization
- AI judges with distinct personalities:
  - Paik Jong Won: Warm, lenient, practical (scores 7-9/10)
  - Anh Sung Jae: Critical, refined, technical (scores 5-7/10)
- Special birthday surprise for Michelle
- Beautiful Korean-themed UI
- Animated loading screen with show GIF

Enjoy your dinner party! 🔥👨‍🍳
