# Vercel Deployment Guide

## Quick Deploy Options

### Option 1: Deploy via Vercel CLI
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel

# Follow the prompts:
# - Set up and deploy? Yes
# - Which scope? (your account)
# - Link to existing project? No
# - Project name: aura-ai-therapy
# - Directory: ./
```

### Option 2: Deploy via GitHub Integration
1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Vercel will auto-detect the settings
6. Click "Deploy"

### Option 3: One-Click Deploy
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/20125A0511/Aura_gemini_playground)

## Environment Variables

After deployment, add your Gemini API key as an environment variable:

1. Go to your Vercel dashboard
2. Select your project
3. Go to Settings > Environment Variables
4. Add: `GEMINI_API_KEY` with your API key value
5. Redeploy

## Custom Domain (Optional)

1. In Vercel dashboard, go to Settings > Domains
2. Add your custom domain
3. Update DNS records as instructed
4. SSL certificate will be automatically provisioned

## Troubleshooting

- **Large video files**: Consider using a CDN or reducing video file sizes
- **API key issues**: Ensure environment variables are set correctly
- **Build errors**: Check that all files are properly committed
