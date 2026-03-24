# 📺 IPTV-PLAYER
🎬 Feature-rich IPTV & media player — HLS, DASH, MP4, MP3, M3U playlists & more. Pure HTML/CSS/JS, no backend needed.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HLS.js](https://img.shields.io/badge/HLS.js-1.5.7-blue?style=for-the-badge)
![DASH.js](https://img.shields.io/badge/DASH.js-latest-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

---

## 🌟 Overview

**IPTV Pro** is a fully client-side, zero-dependency media player built with pure HTML, CSS, and JavaScript. Load any M3U/M3U8 playlist via URL or local file, or paste a direct stream/media link to play instantly — no server, no install, no framework required.

Designed with a **Material Design 3** UI, it works entirely in your browser and supports a wide range of stream protocols and media formats.

---

## ✨ Features

- 🎯 **Universal Playback** — HLS, MPEG-DASH, MP4, MKV, WebM, TS, AVI, MP3, AAC, OGG, FLAC, WAV
- 📋 **M3U / M3U8 Playlist Support** — Load via remote URL or local file
- 🔗 **Direct URL Playback** — Paste any direct media URL and play instantly
- 🌙 **Dark / Light Mode** — Persistent theme toggle
- 🔍 **Search & Filter** — Real-time channel search with category chips
- ⭐ **Favourites** — Star channels and persist them across sessions (localStorage)
- 🕐 **Watch History** — Auto-tracks last 50 played channels
- 🔀 **Sort Options** — Default, A→Z, Z→A, By Type, Favourites First
- ⌨️ **Keyboard Shortcuts** — Navigate channels, mute, fullscreen, sidebar, dark mode, play/pause
- 🖼️ **Picture-in-Picture** — Native PiP support for video streams
- 📡 **Live Stream Detection** — Auto LIVE badge for live streams
- 🔁 **CORS Proxy Fallback** — Auto-retries playlist fetch via allorigins & corsproxy.io
- 📶 **Offline Detection** — Banner alert when network is unavailable
- 📱 **Responsive Design** — Works on desktop and mobile
- 🎨 **Channel Logos** — Auto-loads `tvg-logo` artwork from playlists
- 🏷️ **Rich Metadata** — Parses `tvg-id`, `tvg-name`, `group-title`, `tvg-country`, `tvg-language`
- 🍪 **Custom Headers & Cookies** — Supports pipe-separated `|` header params in stream URLs
- 🔄 **Retry Button** — One-click retry on stream error

---

## 🚀 Quick Start

### Option 1 — Open  THE WEBSITE  URL DIRECTLY IN BROWSER AND USE OR
```
Just open index.html in any modern browser. No build step needed.
```

---

## 🎮 Usage

### Loading a Playlist
1. Paste an M3U/M3U8 playlist URL into the top input bar
2. Click **Load** or press **Enter**
3. Channels populate the sidebar — click any to play

### Playing a Direct Media URL
Paste any direct media URL (MP4, MP3, M3U8, etc.) into the input bar and click **Load** — it auto-detects the type and plays immediately without treating it as a playlist.

### Loading a Local File
Click the 📁 folder icon in the top bar to open a local `.m3u` or `.m3u8` file from your device.

---

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `←` / `→` | Previous / Next channel |
| `Space` | Play / Pause |
| `M` | Mute / Unmute |
| `F` | Fullscreen |
| `S` | Toggle sidebar |
| `D` | Toggle dark mode |
| `Esc` | Close dialogs / drawer |

---

## 📡 Supported Formats

| Type | Formats |
|------|---------|
| **Streaming** | HLS `.m3u8`, MPEG-DASH `.mpd`, RTMP, RTSP |
| **Video** | MP4, MKV, WebM, AVI, MOV, FLV, TS |
| **Audio** | MP3, AAC, OGG, FLAC, WAV, OPUS |
| **Playlist** | M3U, M3U8 |

---

## 🔧 Supported M3U Tags

```m3u
#EXTM3U
#EXTINF:-1 tvg-id="..." tvg-name="..." tvg-logo="..." tvg-country="IN" tvg-language="Hindi" group-title="News",Channel Name
https://stream-url.m3u8

#EXTVLCOPT:http-user-agent=Mozilla/5.0
#EXTVLCOPT:http-referrer=https://example.com

#EXTHTTP:{"User-Agent":"Mozilla/5.0"}

https://stream.mp4|User-Agent=Mozilla&Referer=https://example.com
```

---

## 🛠️ Tech Stack

| Library | Version | Purpose |
|---------|---------|---------|
| [HLS.js](https://github.com/video-dev/hls.js) | 1.5.7 | HLS stream playback |
| [dash.js](https://github.com/Dash-Industry-Forum/dash.js) | latest | MPEG-DASH playback |
| [Material Symbols](https://fonts.google.com/icons) | Rounded | Icons |
| [Google Sans / Roboto](https://fonts.google.com) | — | Typography |

Everything else is **vanilla JS** — no React, no Vue, no bundler.

---

## 🌐 CORS Notice

Some remote streams and playlists may be blocked by browser CORS policy. To bypass this:

- **Chrome:** Install [Allow CORS Extension](https://chromewebstore.google.com/detail/allow-cors-access-control/lhobafahddgcelffkeicbaginigeejlf)
- **Firefox:** Install [CORS Everywhere](https://addons.mozilla.org/en-US/firefox/addon/cors-everywhere/)

The app also automatically tries two CORS proxy fallbacks (`allorigins.win` and `corsproxy.io`) when fetching remote playlists.

---

## 📁 Project Structure

```
IPTV-PLAYER/
└── index.html      # Everything — HTML, CSS, and JS in one self-contained file
```

---

## 🐛 Known Limitations

- RTMP/RTSP streams require a relay or proxy as browsers don't support these protocols natively
- DRM-protected streams (Widevine/PlayReady) are not supported
- Some streams may fail due to CORS restrictions on the stream server side

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

1. Fork the repo
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Bhargav Todimela**  
KL University  
✨ *VibeCoded with [Claude](https://claude.ai) by Anthropic*

---

## ⭐ If you find this useful, give it a star!
