# You N Me AI

A privacy-focused messenger and AI assistant combining biometric 
authentication, end-to-end encryption, and a multilingual conversational AI.

## Live Demo
https://[your-netlify-url].netlify.app

> **Note:** Face ID and camera features require HTTPS and camera permissions. 
> The Anthropic API and (optionally) Firebase need to be configured via the 
> in-app settings panel using your own keys.

## Features

- **Face ID Authentication** using face-api.js with descriptor averaging across 
  multiple samples for improved accuracy
- **AES-256-GCM Encryption** for all messages, using the Web Crypto API
- **Conversational AI Assistant** powered by the Anthropic API (Claude Sonnet)
- **Multilingual Text-to-Speech** in English, Telugu, and Hindi
- **Voice Input** via the Web Speech API
- **Security Snapshots** — captures intruder photo if face verification fails
- **Ghost Mode** — hides conversations from unverified users
- **Animated SVG Robot Avatar** with state-based animations (idle/thinking/speaking)
- **Dark/Light Theme** with full system

## Tech Stack

- Vanilla HTML, CSS, JavaScript (single-file architecture)
- Web Crypto API (AES-GCM)
- face-api.js for face recognition
- MediaDevices API for camera access
- Web Speech API (SpeechSynthesis + SpeechRecognition)
- Anthropic API (browser-side)

## Why I Built This in Vanilla JS

I deliberately avoided frameworks for this project. I wanted to deeply 
understand the underlying browser APIs — encryption, face recognition, 
camera/media streams, speech synthesis — without abstraction. The result 
is a ~2,800-line single-page app that taught me far more about how the 
web platform actually works than any tutorial.

## What I'd Refactor Next

- Split the single HTML file into separate modules (HTML / CSS / JS files)
- Add real-time messaging via Firebase Realtime Database (UI is built; backend wiring is pending)
- Convert to TypeScript for stronger type safety on the crypto layer
- Add unit tests for the encryption and face-matching functions

## Running Locally

1. Clone the repo
2. Open `index.html` in a browser (or serve via `npx serve`)
3. Camera features require HTTPS — use Netlify, Vercel, or `localhost`
4. Add your Anthropic API key via Settings → API Key

## License

MIT
