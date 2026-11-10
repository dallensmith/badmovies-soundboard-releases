# 🎬 Bad Movies Soundboard

A virtual soundboard for Windows, built for streamers and clip-makers. Hit a pad (or a global hotkey) and the sound plays through the output you choose, so it can go straight into OBS, Discord or a stream mix. It replaces a hardware Stream Deck for sound effects.

**[⬇ Download the latest version](https://github.com/dallensmith/badmovies-soundboard-releases/releases/latest)** (`BadMoviesSoundboard-Setup-x.y.z.exe`)

Made for [BadMovies.co](https://badmovies.co). Windows 10/11, 64-bit.

## Install

1. Download `BadMoviesSoundboard-Setup-*.exe` from the [latest release](https://github.com/dallensmith/badmovies-soundboard-releases/releases/latest) and run it.
2. Windows may show a blue **"Windows protected your PC"** screen because the app isn't code-signed. Click **More info → Run anyway**. This only happens on the first install.
3. The app installs for your user only (no admin needed) and opens when finished.

## Updates

The app updates itself. A few seconds after launch (and every few hours while it's open) it checks this repo for a newer version, downloads it quietly, and shows a green **Update vX ready: Restart** button in the header. Click it when you're ready. Your sounds and settings are never touched by an update.

## Features

- **Pads with hotkeys:** click a pad, or give it a global hotkey that works even when the app is in the background. A global **Stop all** hotkey (default `Ctrl+Alt+Esc`) cuts everything.
- **Fade all:** a gentle fade-out of everything playing (`Ctrl+Alt+F`). The **Fade** slider sets the length from 0.5 to 6 seconds (default 1.5).
- **Play actions per pad:** *Play / Stop*, *Play / Overlap*, *Play / Restart*, *Loop / Stop*.
- **Record PC audio:** press **● Record PC audio**, play the sound on your PC, press stop. It records what you hear in stereo with no quality-reducing voice processing, auto-trims the silence, opens the editor, and asks you to name it.
- **Waveform editor:** drag to select, keep or delete a selection, fade in/out, auto-trim, undo.
- **Auto-normalization:** every sound's loudness is measured once and played back at the same level. The **Level** slider changes the overall level and works live while a sound is playing.
- **Pictures on pads:** paste an image (hover a pad and press `Ctrl+V`), drop an image file on it, or use the pad's ⚙ → *Paste image*.
- **Categories:** group pads into tabs. Drag a pad onto a tab to move it.
- **Drag to arrange:** drag pads around to reorder. The **Size** slider makes the tiles bigger or smaller.
- **Choose your output:** send sound to any playback device, such as a virtual audio cable for OBS or Discord.
- **Import from Stream Deck or a folder:** **⇪ Import** reads your Stream Deck profiles (sound buttons, names, button images and folders become pads and categories) or any folder of audio. You pick exactly which sounds to bring in, and ones you already have are unticked automatically.
- **Add sounds easily:** drop audio files (MP3, WAV, OGG, M4A, FLAC) onto the window or use **＋ Add sounds**.

## Quick start

| I want to… | Do this |
|---|---|
| Add a sound I already have | Drag the file onto the window |
| Capture a sound from my PC | **● Record PC audio** → play it → **■ Stop** → name it → **Save** |
| Trim or fade a sound | Hover its pad → **✎** |
| Rename, recolor, set volume, hotkey, action or category | Hover its pad → **⚙** |
| Give a pad a picture | Hover it and press `Ctrl+V` with an image copied |
| Send sound to OBS / Discord | Pick the device in the **Output** dropdown |
| Bring in my Stream Deck sounds | **⇪ Import → From Stream Deck**, tick what you want |
| Stop everything | **■ Stop all** or `Ctrl+Alt+Esc` |
| Fade everything out | **〰 Fade all** or `Ctrl+Alt+F` (length: **Fade** slider) |

To set a hotkey: open the pad's ⚙, click the hotkey button, then press the keys you want.

## Where your stuff is saved

Everything lives in one folder you can see and move: by default `Documents\Bad Movies Soundboard\`.

```
library.json    your pads, order, categories, hotkeys, settings
sounds/         sounds saved as MP3 (256 kbps)
images/         pad pictures saved as WebP
backups/        a daily backup of library.json (last 14 kept)
```

Click **📁 Library** in the app to open the folder or **move it anywhere** (another drive, a cloud-synced folder, a new PC). Moving copies everything, checks it all arrived, and only then removes the old copy. You can also copy the folder by hand.

Because sounds are stored as MP3, re-saving the same sound many times in the editor slowly loses a little quality. A few trims are fine.

## Good to know

- **Record PC audio captures everything your PC is playing**, not one app. Mute other things first.
- Windows may warn about hotkeys it can't register if another program already uses the same combination. The app will tell you which one.
- Only add sounds you have the right to use.

## Troubleshooting

- **No sound in OBS/Discord:** choose the right device in **Output**. Some apps need a virtual audio cable as the pickup device.
- **A sound is too quiet or loud:** use the **Level** slider (all sounds) or the pad's ⚙ volume (one sound).
- **Recording is silent:** make sure something is actually playing on the default Windows output, then try again.
- **Something else broken?** [Open an issue](https://github.com/dallensmith/badmovies-soundboard-releases/issues).

## About

Built with Electron. Installers and updates are published here; the source is kept private.
