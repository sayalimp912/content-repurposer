# AI Content Repurposer

Transform long-form content into platform-optimized posts instantly using AI.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Status](https://img.shields.io/badge/status-active-success.svg)

## 🚀 Overview

AI Content Repurposer is a web application that leverages Large Language Models to automatically transform blog posts, articles, and long-form content into platform-specific formats. Save hours of manual content adaptation with AI-powered text transformation.

Demo - https://content-repurposer-iota.vercel.app/

## ✨ Features

- **Multi-Platform Support**: Convert content to Twitter threads, LinkedIn posts, or Email newsletters
- **Real-Time AI Processing**: Powered by Groq's Llama 3.1 model for fast, high-quality output
- **Smart Formatting**: Each platform gets optimized structure, tone, and length
- **Progress Tracking**: Visual progress bar shows generation status
- **Copy to Clipboard**: One-click copying of repurposed content
- **Character Counting**: Track content length for each platform's limits

## 🛠️ Tech Stack

- **Frontend**: React 18, Tailwind CSS
- **AI/ML**: Groq API (Llama 3.1 8B Instant model)
- **Architecture**: Client-side single-page application
- **Deployment**: Static HTML (no backend required)

## 📋 Prerequisites

- Modern web browser (Chrome, Firefox, Safari, Edge)
- Free Groq API key ([Get one here](https://console.groq.com))

## 🚀 Getting Started

### Installation

1. Clone or download this repository
2. Open `index.html` in your web browser
3. That's it! No installation or build process needed.

### Usage

1. **Get API Key**: Sign up at [console.groq.com](https://console.groq.com) and create a free API key
2. **Enter Key**: Paste your API key in the blue input box at the top
3. **Add Content**: Paste your long-form content in the left textarea
4. **Select Format**: Choose your target platform (Twitter, LinkedIn, or Email)
5. **Repurpose**: Click the "Repurpose Content" button
6. **Copy & Use**: Copy the generated content and paste it on your platform

## 🎯 Use Cases

- **Content Marketers**: Repurpose blog posts across social media
- **Social Media Managers**: Create platform-specific content from one source
- **Bloggers**: Transform articles into promotional social posts
- **Newsletters**: Convert long-form content into email-friendly formats

## 🏗️ Architecture

### How It Works

1. User inputs content and selects target platform
2. App constructs platform-specific prompt with formatting rules
3. Prompt sent to Groq API via RESTful HTTP request
4. Llama 3.1 model processes content and generates optimized output
5. Response parsed and displayed with character count

### API Integration

```javascript
// Example API call structure
fetch('https://api.groq.com/openai/v1/chat/completions', {
  method: 'POST',
  headers: {
    'Authorization': `Bearer ${apiKey}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    model: 'llama-3.1-8b-instant',
    messages: [{ role: 'user', content: prompt }],
    temperature: 0.7,
    max_tokens: 1500
  })
})
```

## 🔒 Security

- **Client-Side API Keys**: Users provide their own API keys (not stored server-side)
- **No Data Storage**: Content is processed in real-time and not saved
- **Direct API Calls**: Communication happens directly between browser and Groq servers

**Note**: For production use, consider implementing a backend proxy to secure API keys and add authentication.

## 🚢 Deployment

### Option 1: Local Use
Simply open `index.html` in any browser - no server needed!

### Option 2: Static Hosting (Recommended)
Deploy to free static hosting services:

**Vercel:**
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

**Netlify:**
- Drag and drop `index.html` to [Netlify Drop](https://app.netlify.com/drop)
- Or connect your GitHub repository

**GitHub Pages:**
```bash
# Push to GitHub
git init
git add .
git commit -m "Initial commit"
git push origin main

# Enable GitHub Pages in repository settings
```

## 🔮 Future Improvements

- [ ] Add more platforms (Instagram captions, TikTok scripts, YouTube descriptions)
- [ ] Tone selector (casual, professional, humorous, persuasive)
- [ ] Save history of repurposed content
- [ ] Batch processing for multiple pieces of content
- [ ] Export to PDF/Word formats
- [ ] Chrome extension version
- [ ] Backend proxy for API key security
- [ ] Analytics dashboard for content performance

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📝 License

This project is licensed under the MIT License - feel free to use it for personal or commercial projects.

## 🙏 Acknowledgments

- **Groq** for providing fast, free LLM inference
- **Meta** for the Llama 3.1 model
- **React** and **Tailwind CSS** for UI framework

## 📧 Contact

Built by Sayali Pendharkar

---

**Note**: This project was developed with assistance from AI coding tools (Claude), demonstrating modern development workflows and AI integration skills.
