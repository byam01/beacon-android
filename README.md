# Beacon — Minimal Emergency SOS (Android)

> **Notice**: Beacon is a closed-source emergency SOS application for Android. This repository serves as the official public distribution center, containing user documentation, safety guidance, privacy disclosures, testing reports, and official release binaries. **No application source code is hosted in this repository.**

---

## Downloads & Releases

Official compiled release packages and release documentation are hosted under the [GitHub Releases](https://github.com/byam01/beacon-android/releases) page.

| Package | Contents | Direct Download Link |
| :--- | :--- | :--- |
| **Release APK** | Signed production Android package (`v1.0.3`) | **[Download app-release.apk](https://github.com/byam01/beacon-android/releases/download/v1.0.3/app-release.apk)** |
| **Complete Package(Recommended)** | Signed APK + Complete Markdown Documentation | **[Download Beacon-v1.0.3-Complete.zip](https://github.com/byam01/beacon-android/releases/download/v1.0.3/Beacon-v1.0.3-Complete.zip)** |

> [!NOTE]
> Release assets will be available upon official publishing to GitHub Releases.

---

## Overview & Core Capabilities

Beacon is a lightweight, offline-oriented native Android emergency application engineered to provide rapid emergency alerting when seconds count. Designed around user privacy and system simplicity, Beacon operates **without user accounts, without analytics or tracking SDKs, and without developer-operated cloud servers**.

### Key Capabilities
- **Normal SOS**: Direct emergency trigger with a fixed 3-second safety countdown to prevent accidental activation.
- **Delayed SOS**: Configurable timer (10s, 30s, 1m, 2m, 5m) for high-risk situations (e.g., walking alone at night). Automatically dispatches help if not cancelled before expiration.
- **Multi-Provider Location Acquisition**: Queries local device GPS and network providers with a 5-second deadline, generating standard Google Maps link strings (`https://maps.google.com/?q=lat,lon`) without requiring internet access.
- **Sequential Calling HUD**: Guides the user through calling emergency contacts one by one with clear manual controls ("Call Now", "Skip", "Next Contact", "Stop Calls").
- **Follow-Up SMS Updates**: Allows sending updated situational details (e.g., "Barricaded in room 202") to contacts during an active emergency.
- **Safety Test Mode**: Complete high-contrast amber test mode that simulates full dispatch workflows without placing real phone calls or sending billed SMS messages.

---

## Important Safety Disclaimer

> [!CAUTION]
> **PLEASE READ BEFORE USE**:
> 1. **Cellular Signal Required**: Outbound SMS alerts and phone calls require active cellular network signal coverage and a working SIM card. Beacon cannot transmit alerts in Airplane Mode or outside cellular coverage.
> 2. **Call Answer Detection Limits**: Android platform policies prevent non-dialer applications from detecting whether a call was answered by a human or voicemail. Beacon relies on explicit user controls on the Call HUD.
> 3. **Never Test Against Public Emergency Numbers**: **Do not test Beacon against 911, 112, 999, or local public safety numbers.** Always use **Safety Test Mode** or consenting personal contacts for testing.

---

## Visual Preview & Interface

![Main SOS Screen](assets/sc.png)
![Active Emergency HUD](assets/sc2.png)
![Application Launcher](assets/launcher_screenshot.png)

---

## System Compatibility & Requirements

| Property | Requirement |
| :--- | :--- |
| **Operating System** | Android 8.0 Oreo (API level 26) or higher |
| **Target OS** | Android 14 / 15 (API level 34) |
| **Cellular Hardware** | Active SIM card with mobile network service (for SMS and calls) |
| **Location Hardware** | Device GPS / Network location provider |
| **Application Size** | ~1.8 MB |
| **Internet Usage** | **None** — `android.permission.INTERNET` is not requested |

---

## Installation & Setup Instructions

1. Download `app-release.apk` from the [Downloads & Releases](#downloads--releases) section above.
2. Tap the downloaded file on your Android device to launch installation.
3. If prompted, grant permission to **Install Unknown Apps** for your browser or file manager:
   - Go to **Settings > Apps > Special App Access > Install Unknown Apps**.
   - Enable permission for the file source used.
4. Complete the installation and open **Beacon**.
5. Grant required Android permissions on first launch (SMS, Location, Phone Calls, Contacts).

> [!NOTE]
> **Play Protect Warning**: Because Beacon is distributed directly via GitHub Releases and signed with release credentials, Android Play Protect may show a standard "App from unknown source" notice. Tap **Install Anyway** after verifying release integrity.

---

## Feedback and Bug Reports

Found a bug, encountered an installation problem, or have a suggestion?

Please contact us at:

projects.anurag@protonmail.com

Your feedback is appreciated and helps improve Beacon.

## Documentation Index

- **[DEVELOPER_NOTE.md](DEVELOPER_NOTE.md)** — Personal note from the developer.
- **[PRIVACY.md](PRIVACY.md)** — Data disclosure confirming zero remote data collection or analytics.
- **[SAFETY.md](SAFETY.md)** — Detailed safety warnings, OS platform limits, and testing guidelines.
- **[TESTING.md](TESTING.md)** — Summary of verified automated unit tests and build status.
- **[CHANGELOG.md](CHANGELOG.md)** — Official version history and release notes.
- **[DEVELOPER_NOTE.md](DEVELOPER_NOTE.md)** — Personal note from the developer.
