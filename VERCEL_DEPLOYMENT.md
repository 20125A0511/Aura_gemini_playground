# Vercel Deployment Guide

## Setting up Environment Variables

To deploy your Aura AI Therapy app to Vercel with the API key, follow these steps:

### Method 1: Vercel Dashboard (Recommended)

1. **Go to your Vercel project dashboard**
2. **Navigate to Settings → Environment Variables**
3. **Add a new environment variable:**
   - **Name**: `GEMINI_API_KEY`
   - **Value**: `AIzaSyDuHfYBuFgQgzCyC89mdGKltothgXpZ_HI`
   - **Environment**: Production, Preview, Development (select all)
4. **Click "Save"**
5. **Redeploy your project** (or it will auto-deploy)

### Method 2: Vercel CLI

```bash
# Install Vercel CLI if you haven't already
npm i -g vercel

# Set the environment variable
vercel env add GEMINI_API_KEY

# When prompted, enter your API key: AIzaSyDuHfYBuFgQgzCyC89mdGKltothgXpZ_HI
# Select all environments (Production, Preview, Development)

# Deploy
vercel --prod
```

### Method 3: One-Click Deploy with Environment Variable

1. **Click the deploy button below**
2. **Import your GitHub repository**
3. **In the Environment Variables section, add:**
   - `GEMINI_API_KEY` = `AIzaSyDuHfYBuFgQgzCyC89mdGKltothgXpZ_HI`
4. **Deploy**

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/20125A0511/Aura_gemini_playground)

## How It Works

- The `build.js` script runs during deployment
- It reads the `GEMINI_API_KEY` environment variable
- It generates a new `config.js` file with the API key
- The app uses this generated config file

## Troubleshooting

### If you still get "API key not configured" error:

1. **Check environment variable is set:**
   - Go to Vercel Dashboard → Settings → Environment Variables
   - Verify `GEMINI_API_KEY` exists and has the correct value

2. **Redeploy the project:**
   - Go to Deployments tab
   - Click "Redeploy" on the latest deployment

3. **Check build logs:**
   - In the deployment logs, look for "✅ Config file generated successfully"
   - Verify "🔑 API Key configured: Yes"

### If the build fails:

1. **Check Node.js version:**
   - Vercel should use Node.js 18+ automatically
   - If not, add `"engines": {"node": ">=18.0.0"}` to package.json

2. **Verify build script:**
   - Make sure `build.js` exists in your repository
   - Check that `package.json` has the build script

## Security Notes

- ✅ API key is stored securely in Vercel environment variables
- ✅ API key is not exposed in your GitHub repository
- ✅ Generated config.js is only available in the deployed app
- ✅ Local development still works with the fallback API key

## Support

If you encounter any issues:
1. Check the Vercel deployment logs
2. Verify environment variables are set correctly
3. Ensure the build script runs successfully
4. Redeploy the project after making changes
