# SlopDrop

Electron desktop app for TikTok/Instagram content creation with AI-generated videos.

## Project Structure

```
├── frontend/       # React + Vite frontend
├── orchestrator/   # Express API server (local orchestration)
├── electron/       # Electron main process files
├── db/            # SQLite database files and schema
└── README.md      # This file
```

## Quick Start

### Prerequisites

- Node.js (v18+ recommended)
- npm

### Installation

1. **Install frontend dependencies:**
   ```bash
   cd frontend
   npm install
   ```

2. **Install orchestrator dependencies:**
   ```bash
   cd orchestrator
   npm install
   ```

### Development

**Start frontend dev server:**
```bash
cd frontend
npm run dev
```

**Start orchestrator API:**
```bash
cd orchestrator
npm start
```

## Environment Variables

Create a `.env` file in the root directory:

```env
WORKER_PORT=8000

DATABASE_URL=sqlite:///./app.db

# OAUTH
TIKTOK_CLIENT_ID=
TIKTOK_CLIENT_SECRET=
INSTAGRAM_CLIENT_ID=
INSTAGRAM_CLIENT_SECRET=
OAUTH_REDIRECT_URI=http://localhost:8000/oauth/callback

# CLOUD VIDEO API
VIDEO_API_KEY=
VIDEO_API_ENDPOINT=https://api.example.com/v1/video/generate

# TTS
TTS_API_KEY=

# ENCRYPTION
ENCRYPTION_KEY_FILE=./.key
```

## Features

- OAuth account linking (TikTok, Instagram)
- Cloud AI video generation
- Video preview and editing
- Direct publishing to platforms

