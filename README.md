<div align="center">

# 🎵 Spotify Lyrics Overlay

**Live, synced lyrics of your Spotify song, floating on top of your games, videos and desktop.**



</div>

<!-- Add screenshots here, for example:
<p align="center"><img src="screenshots/overlay.png" width="720"></p>
-->

---

## ✨ What is it?

A transparent window that sits **on top of everything** and shows the lyrics of the song you're playing in Spotify, line by line, in perfect sync. You can click right through it, so it never gets in your way while you play, watch or work.

## 🚀 Features

| | |
|---|---|
| 🪟 **Click-through overlay** | Always on top. Unlock to move and resize, lock to ignore clicks. |
| 🎛️ **Presets** | Save position, size and look. One for games, one for movies, one for the desktop. |
| 🤖 **Auto-switching** | Presets switch by themselves depending on the active window (game, browser tab, desktop). |
| 🎨 **Fully customizable** | Colors, outline, font, size, alignment, 1 / 3 / 5 lines, opacity, background box. |
| 🔤 **Your own fonts** | Import any TTF, OTF, WOFF or WOFF2 font. |
| 🎬 **14 animations** | Fade, slides, zoom, pop, blur, bounce, flip, flash, typewriter, scroll… |
| ⏱️ **Sync adjustment** | Lyrics too early or late? Nudge them with a hotkey. |
| 🌍 **10 languages** | English, Čeština, Slovenčina, Deutsch, Русский, 中文, Español, Français, Bahasa Indonesia, 日本語 |
| 🧭 **First-run guide** | Walks you through setup step by step. |

## 📥 Install

1. Go to the **[Releases page](https://github.com/Dragouncz/spotify-lyrics-overlay/releases/latest)** and download `Spotify-Lyrics-Overlay-Setup-x.x.x.exe`.
2. Run it. The app installs and starts by itself, and adds a desktop shortcut.
3. Follow the guide that opens (details below).

> **Windows shows a blue "protected your PC" warning?**
> The installer isn't code-signed (certificates cost money). Click **More info → Run anyway**.

## 🔑 First-time setup (2 minutes, only once)

Spotify requires every app to have its own free **Client ID**. The in-app guide walks you through it, and here are the same steps:

1. Open the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard), log in and click **Create app**.
2. Name and description can be anything.
3. In **Redirect URI** paste this exactly and click **Add**:
   ```
   http://127.0.0.1:8888/callback
   ```
4. Under **Which API/SDKs are you planning to use?** tick **Web API**.
5. Accept the terms and click **Save**.
6. Open your new app's **Settings**, copy the **Client ID** and paste it into the app. It logs you in automatically.

Play a song in Spotify and the lyrics appear. 🎉

## 🕹️ How to use

**Tray icon:** click it to open settings, right-click for the quick menu (presets, lock, show/hide, quit).

**Moving the window:** while it's unlocked (dashed frame) drag it with the mouse and resize by dragging the edges. Or use the **Position** tab for exact numbers and a 9-spot quick placement. When you're done, lock it with `Ctrl+Alt+L`.

### ⌨️ Hotkeys

| Shortcut | Action |
|---|---|
| `Ctrl+Alt+L` | Lock / unlock (click-through) |
| `Ctrl+Alt+H` | Hide / show lyrics |
| `Ctrl+Alt+S` | Open settings |
| `Ctrl+Alt+1` … `9` | Switch to preset 1–9 |
| `Ctrl+Alt+P` | Next preset |
| `Ctrl+Alt+↑` / `↓` | Bigger / smaller font |
| `Ctrl+Alt+←` / `→` | Lyrics later / earlier by 250 ms |
| `Ctrl+Alt+Q` | Quit |

### 🎛️ Presets and auto-switching

A preset remembers the window position, size and the whole look. Everything you change is saved into the active preset.

In **Switch when active** you can enter, separated by commas:

| Value | Meaning |
|---|---|
| `chrome.exe` | a program (`.exe` is optional) |
| `desktop` | the Windows desktop |
| `title:YouTube` | text in the window title (browser tabs, Store apps) |

Don't want to type? Click **+ Last window** or **+ Desktop** and it fills it in for you. When you leave to a window with no preset, your previous preset comes back.

Turn on **Hide text in windows that have no preset** (General tab, on by default) and the lyrics only show where you want them.

### 🔤 Custom fonts

Appearance tab → **Import font…**. Your fonts appear under **My fonts**.

## ❓ FAQ & troubleshooting

<details>
<summary><b>Do I need Spotify Premium?</b></summary>

No. Free and Premium both work.
</details>

<details>
<summary><b>I get error 403</b></summary>

In your app on the Spotify Developer Dashboard, open **User Management** and add your own Spotify account (name and email). Then log out and in again in Settings → General.
</details>

<details>
<summary><b>Login does nothing / "Port 8888 cannot be opened"</b></summary>

Another program is using port 8888. Close it and click **Log in again**.
</details>

<details>
<summary><b>"No synced lyrics for this song"</b></summary>

Lyrics come from the free community database [LRCLIB](https://lrclib.net), which doesn't have every song yet. Anyone can add missing lyrics there.
</details>

<details>
<summary><b>The lyrics are a little early or late</b></summary>

Use `Ctrl+Alt+←` / `→` (250 ms per press), or set the offset in Settings → General.
</details>

<details>
<summary><b>It doesn't show in my game</b></summary>

Games in *exclusive fullscreen* can't show overlays. Switch the game to **windowed** or **borderless** mode.
</details>

<details>
<summary><b>How do I uninstall it?</b></summary>

Settings → General → **Uninstall**. You can also delete your settings and Spotify login there. The normal Windows "Apps" list works too.
</details>

## 🔒 Privacy

- The app only talks to **Spotify** (to see which song is playing) and **LRCLIB** (to get lyrics).
- No accounts, no tracking, no data sent to me or anyone else.
- Your settings and login token stay on your PC in `%APPDATA%\spotify-lyrics-overlay\`.
- It uses the official Spotify login (PKCE), so your Spotify password is never seen by the app.

## 💬 Feedback

Found a bug or have an idea? Open an [Issue](https://github.com/Dragouncz/spotify-lyrics-overlay/issues). If you report a bug, include the last lines of `%APPDATA%\spotify-lyrics-overlay\log.txt` (remove anything private).

---

<div align="center">

Free to use. Not affiliated with, endorsed by or sponsored by Spotify.
Lyrics provided by [LRCLIB](https://lrclib.net).

</div>
