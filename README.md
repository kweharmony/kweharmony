# Hey! 👋 I'm sesitskii

## About Me

Just a developer who loves building stuff that actually works and looks good doing it. I'm all about creating practical solutions that make life easier - whether it's transcription tools, database systems, or just beautiful interfaces.

<br/>

<div align="center">
  <img src="konata-lucky-star.gif" width="400">
</div>

## My Toolkit

Here's what I work with on a daily basis:

**Core Languages:**  
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)

**Frontend Vibes:**  
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

**Backend & Data:**  
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Desktop:**  
![Tauri](https://img.shields.io/badge/Tauri-24C8DB?style=for-the-badge&logo=tauri&logoColor=white)

## What I've Been Building

### [MindeSync](https://github.com/kweharmony/student-ai-assistant) 🎓
**Turn lecture recordings into ready-to-use study materials with AI**

A full-stack platform that takes a lecture audio file and turns it into clean, structured notes. Upload audio → it's transcribed locally with Whisper → an LLM cleans it up and generates summaries, terms, questions and cheat sheets → export or publish to your group's shared knowledge base. Built as a team project where I led development and handled the frontend, infra and UI/UX.

**What it does:**
- **Local transcription** — audio (up to 100MB, any popular format) → text via OpenAI Whisper on a separate GPU worker, audio never leaves to third parties
- **7 AI modes** — short & detailed summaries, key terms, self-check questions, topic deep-dives, cheat sheets, and inline fragment explanations
- **Smart long-text handling** — Multi-Step Generation splits a lecture into themes and generates them in parallel to beat the LLM output limit
- **Shared catalog** — faculty → direction → stream → course → semester → discipline hierarchy, with moderation by group heads and admins
- **Real-time whiteboards** (Excalidraw) — collaborative drawing with live cursors over WebSocket + Redis
- **Export** to PDF, DOCX, TXT and Markdown; rich editor with KaTeX math rendering
- Roles (student / teacher / admin), free/pro tiers with rolling-window quotas

**Tech behind it:**
- React 18 + TypeScript + Tailwind + Framer Motion + TipTap editor
- FastAPI + SQLAlchemy (async) + PostgreSQL + Redis + Alembic
- OpenAI Whisper (CPU/CUDA) on a standalone polling worker with heartbeat & retry
- LLM via OpenAI-compatible API; Node + Playwright/Chromium PDF service
- Docker Compose (6 services) behind Nginx, GitHub Actions CI/CD

**Live:** [mindesync.ru](https://mindesync.ru)

Drop in a recording, get a polished summary, and share it with your whole stream.

### [Mestia](https://github.com/kweharmony/mestia) ▼
**Cross-platform desktop app for downloading videos & organizing a media library**

A native desktop app that wraps `yt-dlp` in a clean, themeable interface - download video or audio from 1800+ sites, then keep everything tidy in a built-in media library with its own player. Fast, lightweight (Rust core), works offline.

**What it does:**
- **Downloads** video (1080p…360p) or audio (MP3/WAV/FLAC) from YouTube, Rutube, VK, TikTok, Vimeo and 1800+ sites
- **Playlists** - whole list or a range, into their own folder
- **Parallel background downloads** with a queue, cancel, and resume of interrupted ones
- **Media library** - folders, drag-and-drop, multi-select (marquee like Explorer), search, real-time file watching
- **Built-in video & audio player** with a detachable always-on-top mini-window
- 8 themes, system tray, desktop notifications, custom covers

**Tech behind it:**
- Tauri v2 (Rust) + React + TypeScript
- Tailwind CSS v4 + SQLite (tauri-plugin-sql)
- yt-dlp + ffmpeg bundled as sidecar binaries
- GitHub Actions auto-building installers for Windows / macOS / Linux

**Downloads:** [Releases](https://github.com/kweharmony/mestia/releases/latest) - Windows (.exe/.msi), macOS (.dmg), Linux (.deb/.rpm/.AppImage).

Choose a format, paste a link, and it just works - even watch in a floating mini-player while you do other things.

### [Salpa](https://github.com/kweharmony/salpa) 🔄
**Browser-based file converter that respects your privacy**

A web app for converting files between different formats - images, documents, audio, and video. The cool part? Everything happens in your browser. No uploads, no servers, no tracking. Your files never leave your device.

**What it does:**
- **Images**: PNG ↔ JPG ↔ WebP ↔ BMP ↔ ICO (and more)
- **Documents**: TXT ↔ MD ↔ JSON ↔ CSV ↔ HTML ↔ XML
- **Audio**: MP3 ↔ WAV, plus OGG/FLAC/AAC support
- **Video**: MP4 ↔ WebM ↔ AVI ↔ MOV (using ffmpeg.wasm)

**Tech behind it:**
- Next.js 16 + React 19 + TypeScript
- Canvas API for images, Web Audio API for audio
- ffmpeg.wasm for video processing (25MB, loads on demand)
- shadcn/ui + Tailwind for the interface

**Live demo:** [salpa.vercel.app](https://salpa.vercel.app/)

No file size limits, no watermarks, completely free. Just drag, convert, download.

### [University Timetable](https://github.com/kweharmony/university-timetable)
Simple schedule tracker.

<div align="center">

</div>
