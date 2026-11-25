<div align="center">

# Downloader Ultra

### Download anything. Beautifully.

A fast, minimal video, music and file downloader for Android, in calm black and white.

[![Latest release](https://img.shields.io/github/v/release/Paradox-ultra/downloader-ultra?label=latest&style=for-the-badge&color=111111)](https://github.com/Paradox-ultra/downloader-ultra/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/Paradox-ultra/downloader-ultra/total?style=for-the-badge&color=111111)](https://github.com/Paradox-ultra/downloader-ultra/releases)
![Android 8.0+](https://img.shields.io/badge/Android-8.0%2B-111111?style=for-the-badge&logo=android&logoColor=white)

### [⬇ Download Downloader Ultra](https://github.com/Paradox-ultra/downloader-ultra/releases/latest)

</div>

---

## Why Downloader Ultra

- **The quality the creator uploaded.** YouTube in up to 4K and 8K at 60 fps, with video and audio joined into one file. *Best available* is picked for you; choose any other quality before the download starts.
- **Whole playlists in one tap.** YouTube and YouTube Music playlists, plus Spotify playlists, albums and songs, matched to YouTube Music and saved as tagged songs with cover art.
- **1000+ sites.** Instagram, TikTok, X, Facebook, Vimeo, Reddit and [many more](https://github.com/yt-dlp/yt-dlp/blob/master/supportedsites.md), powered by a built-in yt-dlp that keeps itself up to date.
- **Any file, fast.** Up to 16 connections per download, pause and resume anytime, and smart handling of Google Drive, Dropbox, OneDrive, MediaFire and Gofile links.
- **Your choice of extras.** Video or audio only, thumbnail, captions and embedded cover art, all as simple checkboxes.
- **Soft, minimal design.** A black-and-white look with thumbnails and quality badges on every download, and four themes: **Light**, **Dark**, **AMOLED black** and *Follow system*.
- **Private by design.** No account, no ads, no tracking. Files go straight to `Download/Downloader Ultra`.

## How it works

1. Copy a link from any app (or use **Share → Downloader Ultra**).
2. Open the app and tap **Paste link**.
3. Pick video or audio and the quality, then tap **Download**.

## Install

1. Open the **[latest release](https://github.com/Paradox-ultra/downloader-ultra/releases/latest)** and download the APK for your phone under **Assets**:
   - **`…_arm64-v8a.apk`**: almost every phone from 2017 on. Pick this if unsure.
   - **`…_armeabi-v7a.apk`**: older or budget phones with a 32-bit system.
2. Open the downloaded file. If Android asks, allow your browser or file manager to **install unknown apps**.
3. Tap **Install**. New versions install over the old one and keep your downloads; the app tells you when an update is out.

**Requirements:** Android 8.0 (Oreo) or newer.

## Troubleshooting

| Problem | Fix |
|---|---|
| **"App not installed"** | Another copy with the same name but a different signature is installed. Uninstall it (also from Dual Apps / Secure Folder / work profile), then install again. |
| **"Harmful app blocked" / "Blocked by Play Protect"** | Tap **More details → Install anyway**. Play Protect warns about any app from outside the Play Store. |
| **"There was a problem parsing the package"** | The download was cut off. Download it again and check it with the steps below. |
| **Install button greyed out** | Close screen overlay or bubble apps (screen dimmers, chat heads) and try again. |

## Verify your download (optional)

Each release includes `SHA256SUMS.txt`. Put it next to the APK and run:

```sh
sha256sum -c SHA256SUMS.txt
```

It should print `OK`.

## About

Downloader Ultra is free and open source under the [GPL-3.0](LICENSE). The source code is at **[Paradox-ultra/paradox-downloader-source](https://github.com/Paradox-ultra/paradox-downloader-source)**. This repository hosts the official signed release builds; please download the app only from this page.

<details>
<summary>For maintainers: publishing a build</summary>

Run **Actions → Attach release asset → Run workflow** with:

- `tag`: the release tag, e.g. `v4.5.1` (a release is created if it doesn't exist)
- `apk_url`: one or more temporary download URLs, space-separated, in order
- `apk_name`: e.g. `Downloader_Ultra_v4.5.1_arm64-v8a.apk`; run once per APK
- `apk_sha256`: the SHA-256 of the full APK

The workflow joins the parts, checks the hash, and uploads the APK with `SHA256SUMS.txt`.

</details>
