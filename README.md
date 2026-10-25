## Hey! 👋 I'm sesitskii

Just a developer who loves building stuff that actually works and looks good doing it. I'm all about creating practical solutions that make life easier - whether it's a media app that runs on desktop and phone, a privacy-first file converter, or just a beautiful interface.

<table>
<tr>
<td width="40%" align="center">

<img src="konata-lucky-star.gif" width="300">

</td>
<td width="60%" valign="top">

## 🛠️ My Toolkit

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

**Desktop & Mobile:**  
![Tauri](https://img.shields.io/badge/Tauri-24C8DB?style=for-the-badge&logo=tauri&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)

</td>
</tr>
</table>

## What I've Been Building

### Mestia ▼
**Download. Keep. Watch. — a video & music downloader with its own media library, for desktop and Android**

<a href="https://kweharmony.github.io/Mestia/?lang=en"><img src="https://raw.githubusercontent.com/kweharmony/Mestia/main/docs/media/promo.en.webp" width="720" alt="Mestia promo: paste a link, download, watch, share nearby" /></a>

A native app that wraps yt-dlp in a clean, themeable interface - download video or audio from 1800+ sites, keep everything tidy in a built-in library with its own player, and share it with your other devices over Wi-Fi. No accounts, no telemetry, everything stays on your device.

**What it does:**
- **Downloads** video (up to 4K) or audio (MP3/M4A/FLAC/WAV) from YouTube, VK, Rutube, TikTok, SoundCloud and 1800+ sites; Spotify & Apple Music links are matched on YouTube
- **One progress for the final file** - video and audio streams are merged in a hidden temp folder, only the finished file lands in the library; queue, cancel, resume
- **Media library & player** - folders, drag-and-drop, search, a player with overlay controls and a music-card mode, remembers where you stopped
- **Nearby** - send files between desktop and phone and **watch together** in sync, straight over your Wi-Fi, no internet needed
- **Android** - media notification with cover art, playback with the screen off, download progress in the shade, “Share → Download with Mestia”
- **Ctrl+K** command palette, 8 themes with a matching app icon (even the Android launcher icon), RU / EN / 中文 UI

**Tech behind it:**
- Tauri v2 (Rust) + React 18 + TypeScript + Tailwind CSS v4 + Framer Motion
- SQLite, yt-dlp + ffmpeg bundled as sidecars; on Android a Kotlin plugin over youtubedl-android with MediaSession & foreground services
- Axum HTTP/WebSocket + UDP discovery for the LAN features, NTP-style clock sync for watch-together
- GitHub Actions building signed installers and APKs, auto-updates on desktop

**Get it:** [website](https://kweharmony.github.io/Mestia/?lang=en) · [releases](https://github.com/kweharmony/Mestia/releases/latest) - Windows (.exe), Linux (AppImage / .deb / Flatpak), Android (APK) · [source](https://github.com/kweharmony/Mestia)

Paste a link, grab a coffee, and it's in your library - on your laptop and your phone.

### Salpa 🔄
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

**Live demo:** [salpa.vercel.app](https://salpa.vercel.app)

No file size limits, no watermarks, completely free. Just drag, convert, download.
