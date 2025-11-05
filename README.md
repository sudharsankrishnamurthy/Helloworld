# Node.js Hello World App

A simple Node.js web application that displays a Hello World page with an AI chat feature.

## Features

- Express web server
- Beautiful responsive UI with gradient background
- Animated Hello World message
- Mobile-friendly design
- **AI Chat powered by Google Gemini** - Chat with AI directly from the app!

## Local Development

```bash
npm install
npm start
```

The app will run on http://localhost:3000

## Setting Up AI Chat

To enable the AI chat feature, you need a Google Gemini API key:

### Get Your API Key:

1. Go to https://makersuite.google.com/app/apikey
2. Sign in with your Google account
3. Click "Create API Key"
4. Copy your API key (starts with `AIza...`)

### For Local Development:

Create a `.env` file in the project root:
```bash
GEMINI_API_KEY=your_api_key_here
```

### For Render.com Deployment:

1. In your Render dashboard, go to your web service
2. Click "Environment" in the left sidebar
3. Click "Add Environment Variable"
4. Add:
   - **Key**: `GEMINI_API_KEY`
   - **Value**: Your Gemini API key
5. Click "Save Changes"
6. Render will automatically redeploy with the new environment variable

## Deploy to Render.com (Free)

This app is ready to deploy to Render.com for free!

### Steps:

1. Go to https://render.com and sign up (free)
2. Click "New +" and select "Web Service"
3. Connect your GitHub account
4. Select this repository
5. Render will auto-detect the settings, or use these:
   - Build Command: `npm install`
   - Start Command: `npm start`
6. **Before clicking "Create"**, scroll down to "Environment Variables" and add:
   - **Key**: `GEMINI_API_KEY`
   - **Value**: Your Gemini API key (from above)
7. Click "Create Web Service"
8. Wait 2-3 minutes for deployment
9. Your app will be live at: `https://your-app-name.onrender.com`

### Using the Chat Feature:

1. Visit your deployed app
2. Click the purple chat button (💬) in the bottom-right corner
3. Type your message and press Enter or click Send
4. Chat with the AI powered by Google Gemini!

## Files

- `server.js` - Express server with Gemini AI chat endpoint
- `index.html` - Main HTML page with chat UI
- `package.json` - Dependencies (Express + Gemini AI)
- `render.yaml` - Render deployment config
- `.env.example` - Environment variable template
- `.gitignore` - Git ignore file (includes .env)
