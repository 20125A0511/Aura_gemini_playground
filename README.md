# Aura AI Therapy Assistant

A professional AI-powered therapy assistant that provides evidence-based therapeutic support through a structured 5-stage process.

## Features

- **5-Stage Therapeutic Process**: Assessment, Intervention, Change/Action, Evaluation, and Termination
- **Evidence-Based Approach**: Built on CBT, DBT, and mindfulness techniques
- **Professional UI**: Modern, responsive design with glass morphism effects
- **Dynamic Background**: Rotating video backgrounds for visual appeal
- **Memory Integration**: AI remembers conversation history and builds therapeutic rapport
- **Emergency Resources**: Built-in crisis support and helpline information

## Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Styling**: Tailwind CSS
- **AI Integration**: Google Gemini API
- **Deployment**: Vercel-ready static site

## Setup Instructions

### 1. Get a Gemini API Key

1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Sign in with your Google account
3. Click "Create API Key"
4. Copy your API key

### 2. Configure the Application

1. Copy `config.js.example` to `config.js`:
   ```bash
   cp config.js.example config.js
   ```

2. Open `config.js` and replace `YOUR_API_KEY_HERE` with your actual Gemini API key:
   ```javascript
   const CONFIG = {
       GEMINI_API_KEY: 'your-actual-api-key-here'
   };
   ```

### 3. Deploy to Vercel

1. Install Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. Deploy:
   ```bash
   vercel
   ```

3. Or connect your GitHub repository to Vercel for automatic deployments.

## Project Structure

```
├── index.html              # Landing page
├── therapy_static.html     # Chat interface
├── config.js.example      # API key template
├── logo.png               # Application logo
├── media/                 # Background videos
│   ├── 1.mp4
│   ├── 2.mp4
│   ├── 3.mp4
│   └── 4.mp4
├── vercel.json            # Vercel configuration
├── package.json           # Project metadata
└── README.md              # This file
```

## 5-Stage Therapeutic Process

1. **Assessment/Introduction** (Sessions 1-6): Building trust and gathering information
2. **Intervention** (Sessions 7-12): Setting goals and learning strategies
3. **Change/Action** (Sessions 13-20): Implementing new behaviors
4. **Evaluation** (Sessions 21-25): Assessing progress and outcomes
5. **Termination** (Session 26+): Planning for the future

## Important Disclaimer

Aura is an AI therapy assistant designed to complement, not replace, licensed mental health care. While our platform uses evidence-based therapeutic techniques, it cannot provide medical diagnoses, prescribe medications, or handle emergency situations.

**Emergency Support**: If you're experiencing thoughts of self-harm, suicide, or other mental health emergencies, please contact emergency services (911) or the National Suicide Prevention Lifeline (988) immediately.

## License

MIT License - see LICENSE file for details.

## Contributing

This project is for educational and supportive purposes. Please ensure any contributions maintain the therapeutic integrity and safety standards of the application.
