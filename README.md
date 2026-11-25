<div align="center">

# Downloader Ultra

**A video, music and file downloader for Android.** Formerly *Paradox Downloader*.

[![Latest release](https://img.shields.io/github/v/release/Paradox-ultra/paradox-downloader?label=latest&style=for-the-badge)](https://github.com/Paradox-ultra/paradox-downloader/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/Paradox-ultra/paradox-downloader/total?style=for-the-badge)](https://github.com/Paradox-ultra/paradox-downloader/releases)
![Android 8.0+](https://img.shields.io/badge/Android-8.0%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)

### [⬇ Download the latest APK](https://github.com/Paradox-ultra/paradox-downloader/releases/latest)

</div>

---

## Install

1. Open the **[latest release](https://github.com/Paradox-ultra/paradox-downloader/releases/latest)** and download the APK for your phone under **Assets**:
   - **`…_arm64-v8a.apk`**: almost every phone from 2017 on. Pick this if unsure.
   - **`…_armeabi-v7a.apk`**: older or budget phones with a 32-bit system. Use it if the other one says "App not installed".
2. Open the downloaded file. If Android asks, allow your browser or file manager to **install unknown apps**.
3. Tap **Install**.

**Requirements:** Android 8.0 (Oreo) or newer.

## Updating

**Coming from v4.2 or older?** Uninstall the old app. From v4.3.1 the app has a new signing key and a new app ID (`bot.paradox.downloader.app`), so it installs as a separate app and can't update the old one.

From v4.3.1 on, install new versions over the old one: your downloads and settings are kept.

## Verify your download (optional)

Each release lists the APK's SHA-256 in its notes and in `SHA256SUMS.txt`. To check the APK was not corrupted or changed, put both files in one folder and run:

```sh
sha256sum -c SHA256SUMS.txt
```

It should print `OK`. On Windows: `certutil -hashfile Downloader_Ultra_v4.5_arm64-v8a.apk SHA256`, then compare with the hash in the release notes.

## Troubleshooting

| Problem | Fix |
|---|---|
| **"App not installed"** | An old version (v4.2 or older) or a copy signed by someone else is still installed. Uninstall it (also from Dual Apps / Secure Folder / work profile), then install the APK from this page. |
| **"Harmful app blocked" / "Blocked by Play Protect"** | Tap **More details → Install anyway**. Don't tap *OK*: that cancels the install. Play Protect warns about apps from outside the Play Store. |
| **"There was a problem parsing the package"** | The download was cut off. Download it again and check it with the steps above. |
| **Install button greyed out** | Close any screen overlay or bubble apps (screen dimmers, chat heads), then try again. |

## What's new in v4.5

- **New name: Downloader Ultra**, with a new icon (a white circle with a rounded download arrow).
- **A soft black-and-white design.** Calm monochrome colours, the Inter font, rounded cards and pill-shaped buttons.
- **Theme setting:** Settings → *Theme* → Follow system, Light, Dark or **AMOLED black** (pure black, kind to OLED screens and battery).
- **New home screen:** a live status line ("2 downloading · 8.4 MB/s"), a big link box and a one-tap **Paste link** button.
- **Thumbnails on your downloads.** Cards show the video thumbnail or album art, the quality you picked (e.g. `2160p60 · VP9`) and a percentage.
- **Bigger quality picker** with a large preview and the video length.
- Finished files now save to `Download/Downloader Ultra`.

## v4.4

- **Pick the quality before every download.** Paste a video link and choose Video or Audio only, then the quality. *Best available* (selected by default) saves the highest quality the creator uploaded (up to 4K/8K), with video and audio joined into one file.
- **Thumbnail and captions.** Tick *Save thumbnail* / *Captions* to save them next to the video; for music, *Add cover art* embeds the artwork in the song.
- **yt-dlp built in.** Instagram, Facebook, X, TikTok, Vimeo, Reddit and [1000+ other sites](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md). It updates itself once a day.
- **Whole playlists in one tap.** YouTube and YouTube Music playlists download every track. Spotify playlists, albums and songs work too: Spotify's audio is DRM-protected, so each song is found by name on YouTube Music (up to about 100 songs per Spotify list).
- **Fix:** a download no longer gets stuck on *Downloading* when one part of it fails.
- One APK per CPU type to keep the download small (see *Install*).

## v4.3.1

- **Rebuilt from the ground up.** New Material 3 design, dark mode, and a smooth download list.
- **Faster, sturdier downloads.** Up to 16 connections per file; resume works after pausing, closing the app or losing signal.
- **Files land in Downloads** with proper names and extensions.
- **Better link support:** Google Drive large files, Gofile, Dropbox, OneDrive, MediaFire and mirror pages.
- **17 bugs fixed**, including stuck *Queued* jobs, wrong sizes and battery-draining animations.
- **New app ID and signing key.** See *Updating* above.

**v4.2:** Automatic update check. When a new version is out, an *Update available* card shows when you open the app, with *Download*, *Later* and *Skip this version*. Checked at most every 12 hours. No tracking, no new permissions.

**v4.1:** WhatsApp channel welcome card on launch, with *Join channel*, *Later* and *Don't show again*.

See [all releases](https://github.com/Paradox-ultra/paradox-downloader/releases) for older changes.

## About this repository

This repository holds release builds only; the source code is not published here. Please download the app only from this page.

<details>
<summary>For maintainers: publishing a build</summary>

Run **Actions → Attach release asset → Run workflow** with:

- `tag`: the release tag, e.g. `v4.5` (a release is created if it doesn't exist)
- `apk_url`: one or more temporary download URLs, space-separated, in order (tmpfiles.org share and download-page links are followed automatically)
- `apk_name`: e.g. `Downloader_Ultra_v4.5_arm64-v8a.apk`; run once per APK
- `apk_sha256`: the SHA-256 of the full APK

The workflow joins the parts, checks the hash, and uploads the APK with `SHA256SUMS.txt`.

</details>
