<div align="center">

# Paradox Downloader

**A video and file downloader for Android.**

[![Latest release](https://img.shields.io/github/v/release/Paradox-ultra/paradox-downloader?label=latest&style=for-the-badge)](https://github.com/Paradox-ultra/paradox-downloader/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/Paradox-ultra/paradox-downloader/total?style=for-the-badge)](https://github.com/Paradox-ultra/paradox-downloader/releases)
![Android 8.0+](https://img.shields.io/badge/Android-8.0%2B-3DDC84?style=for-the-badge&logo=android&logoColor=white)

### [⬇ Download the latest APK](https://github.com/Paradox-ultra/paradox-downloader/releases/latest)

</div>

---

## Install

1. Open the **[latest release](https://github.com/Paradox-ultra/paradox-downloader/releases/latest)** and download the `.apk` file under **Assets** (for example `Paradox_Downloader_v4.2.apk`).
2. Open the downloaded file. If Android asks, allow your browser or file manager to **install unknown apps**.
3. Tap **Install**.

**Requirements:** Android 8.0 (Oreo) or newer.

## Updating

Install the new APK over the old one. All official builds are signed with the same key, so your downloads and settings are kept.

## Verify your download (optional)

Each release lists the APK's SHA-256 in its notes and in `SHA256SUMS.txt`. To check the APK was not corrupted or changed, put both files in one folder and run:

```sh
sha256sum -c SHA256SUMS.txt
```

It should print `OK`. On Windows: `certutil -hashfile Paradox_Downloader_v4.2.apk SHA256`, then compare with the hash in the release notes.

## Troubleshooting

| Problem | Fix |
|---|---|
| **"App not installed"** | You have a copy signed by someone else. Uninstall it, then install the APK from this page. Your data from that copy will not carry over. |
| **"Blocked by Play Protect"** | Tap **More details → Install anyway**. This shows for apps installed outside the Play Store. |
| **"There was a problem parsing the package"** | The download was cut off. Download it again and check it with the steps above. |
| **Install button greyed out** | Close any screen overlay or bubble apps (screen dimmers, chat heads), then try again. |

## What's new in v4.2

- **Automatic update check.** When a new version is out, an *Update available* card shows when you open the app, with *Download*, *Later* and *Skip this version*. Checked at most every 12 hours. No tracking, no new permissions.

**v4.1:** WhatsApp channel welcome card on launch, with *Join channel*, *Later* and *Don't show again*.

See [all releases](https://github.com/Paradox-ultra/paradox-downloader/releases) for older changes.

## About this repository

This repository holds release builds only; the source code is not published here. Please download the app only from this page.

<details>
<summary>For maintainers: publishing a build</summary>

Run **Actions → Attach release asset → Run workflow** with:

- `tag`: the release tag, e.g. `v4.3` (a release is created if it doesn't exist)
- `apk_url`: one or more temporary download URLs, space-separated, in order (tmpfiles.org share links are converted automatically)
- `apk_name`: e.g. `Paradox_Downloader_v4.3.apk`
- `apk_sha256`: the SHA-256 of the full APK

The workflow joins the parts, checks the hash, and uploads the APK with `SHA256SUMS.txt`.

</details>
