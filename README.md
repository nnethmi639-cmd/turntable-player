# 🎧 Turntable — Music Player

A single-file, vinyl-themed web music player. No build tools, no backend — just open the HTML file and play your local music library right in the browser, with a full set of player features baked in.

## ✨ Features

- 🎨 **Vinyl turntable UI** — a spinning disc and tonearm that animate with playback, with a per-track accent color
- ▶️ Play / pause, next / previous, seek bar, and volume control
- 🔀 Shuffle and 🔁 repeat (off / repeat all / repeat one)
- 📃 **Playlist management** — add local audio files, remove tracks, drag-and-drop reordering, search, and favorite tracks
- 🗂️ **Multiple playlists** — create and switch between playlists (session-only)
- ⏭️ **Play queue** — queue up tracks to play next
- 🕘 **Recently played history**
- 📤 **Export / import** a playlist as JSON
- 🎚️ **Bass & treble EQ** plus a **crossfade** toggle, powered by the Web Audio API
- 📊 Live **audio visualizer** (frequency bars)
- 📝 Per-track **lyrics** panel
- ⏰ **Sleep timer**
- ⌨️ **Keyboard shortcuts** — space to play/pause, arrow keys to skip, `M` to mute, `L` to favorite, `?` for the shortcuts overlay
- 💾 **State persistence** — remembers volume, current track, favorites, shuffle/repeat mode, and lyrics via `localStorage`
- 🔑 Simple login gate (name/guest — client-side only, no real authentication/backend)
- 📱 PWA-ready (manifest link + apple touch icon) and fully responsive, with a mini-player bar

## 🛠️ Tech Stack

Pure **HTML5, CSS3, and vanilla JavaScript** — everything lives in a single `.html` file. No frameworks, no build step, no dependencies.

- HTML5 `<audio>` for playback
- Web Audio API for the EQ, crossfade, and visualizer
- `localStorage` for saving player state
- Google Fonts (Fraunces, Inter, JetBrains Mono)

## 📁 Project Structure

```
turntable-music-player/
└── music-player.html   # everything — markup, styles, and script — in one file
```

## 🚀 Getting Started

No installation or build step needed.

1. Download or clone this repository.
2. Open `music-player.html` directly in your browser (double-click, or drag it into a browser window).
3. Log in with any name (or continue as guest) and click **+ Add song** to load audio files from your device.

> Because it's a self-contained HTML file, you can also just double-click it — no local server required.

## 🎧 Usage

- **Add music**: click **+ Add song** and select audio files from your device.
- **Control playback**: use the transport buttons, or space bar to play/pause and arrow keys to skip tracks.
- **Organize**: drag tracks to reorder, star tracks to favorite them, use the search box to filter, or filter to favorites only.
- **Queue**: click the queue icon on a track to play it next without disrupting your current playlist order.
- **Playlists**: switch or create playlists from the playlist selector; export the current one as JSON to back it up, and import it later.
- **Sound**: open the tools panel to adjust bass/treble, toggle crossfade, or set a sleep timer.
- **Shortcuts**: press `?` any time to see the full keyboard shortcut list.

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play / pause |
| `←` / `→` | Previous / next track |
| `M` | Mute / unmute |
| `L` | Favorite / unfavorite current track |
| `?` | Toggle shortcuts overlay |

## ⚠️ Notes

- Tracks added via **+ Add song** are loaded from local files in your browser session (via `URL.createObjectURL`) — they aren't uploaded anywhere, but they also won't persist after a page refresh unless you re-add them. Exported/imported playlists store file references as JSON, not the audio itself.
- The login screen is a UI flow only — it does not authenticate against any server or store credentials.

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m "Add your feature"`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the [MIT License](LICENSE).

## 👤 Author

- **Your Name** — [GitHub](https://github.com/your-username)
