# BEACON — Minimal Emergency SOS (Android)

> **Notice**: BEACON is a closed-source emergency SOS application for Android. This repository serves as the official public distribution center, containing user documentation, safety guidance, privacy disclosures, testing reports, and official release APKs. **No application source code is hosted in this repository.**

---

## Overview & Core Features

BEACON is a lightweight, reliable, offline-first native Android emergency application engineered to provide rapid emergency alerting when seconds count. Designed around absolute reliability and user privacy, BEACON operates with **zero accounts, zero analytics, zero advertising, zero remote servers, and 100% offline autonomy**.

### Key Capabilities
- **Normal SOS**: Direct emergency trigger with a fixed 3-second safety countdown to prevent accidental activation.
- **Delayed SOS**: Configurable timer (10s, 30s, 1m, 2m, 5m) for high-risk situations (e.g., walking alone at night). Automatically dispatches help if not cancelled before expiration.
- **Offline Location Acquisition**: Multi-provider location engine that generates standard Google Maps coordinate links (`https://maps.google.com/?q=lat,lon`) locally without internet connectivity.
- **Sequential Calling HUD**: Guides the user through calling emergency contacts one by one with clear manual controls ("Call Now", "Skip", "Next Contact", "Stop Calls").
- **Tactical Follow-up SMS**: Allows sending updated situational details (e.g., "Barricaded in room 202") to contacts during an active emergency.
- **Safety Test Mode**: Complete high-contrast amber test mode that simulates full dispatch workflows without placing real phone calls or sending billed SMS messages.

---

## System Compatibility & Requirements

| Property | Requirement |
| :--- | :--- |
| **Operating System** | Android 8.0 Oreo (API level 26) or higher |
| **Target OS** | Android 14 / 15 (API level 34) |
| **Network Hardware** | Active SIM card with cellular network service (for SMS/Calls) |
| **Location Hardware** | Device GPS / Network location provider |
| **Application Size** | ~1.8 MB |
| **Network Usage** | **0 KB (100% Offline)** — No internet permissions requested |

---

## Installation & Setup Instructions

### Downloading Approved Releases
Official compiled Android Application Packages (APKs) are available directly under the **[GitHub Releases](https://github.com/beacon-android/releases)** section of this repository.

### Installing the APK on Android
1. Download the latest `app-release.apk` from the Releases section.
2. Tap the downloaded file on your Android device.
3. If prompted, grant permission to **Install Unknown Apps** for your browser or file manager:
   - Go to **Settings > Apps > Special App Access > Install Unknown Apps**.
   - Enable permission for the app used to download the file.
4. Complete the installation and launch **BEACON**.
5. Grant required Android permissions on first launch (SMS, Location, Phone Calls, Contacts).

> [!NOTE]
> **Play Protect / Unknown Sources Warning**: Because BEACON is distributed directly via GitHub Releases and signed with release credentials, Android may show a standard "App from unknown source" warning during installation. You can tap **Install Anyway** after verifying the official release checksums published in [CHANGELOG.md](file:///D:/tempo/beacon---minimal-emergency-sos/beacon-android/CHANGELOG.md).

---

## Documentation Index

- **[PRIVACY.md](file:///D:/tempo/beacon---minimal-emergency-sos/beacon-android/PRIVACY.md)** — Detailed privacy disclosure confirming zero data collection or transmission.
- **[SAFETY.md](file:///D:/tempo/beacon---minimal-emergency-sos/beacon-android/SAFETY.md)** — Emergency warnings, OS limits, and testing guidelines.
- **[TESTING.md](file:///D:/tempo/beacon---minimal-emergency-sos/beacon-android/TESTING.md)** — Summary of verified automated unit tests and build status.
- **[CHANGELOG.md](file:///D:/tempo/beacon---minimal-emergency-sos/beacon-android/CHANGELOG.md)** — Official release notes and version history.
- **[DEVELOPER_NOTE.md](file:///D:/tempo/beacon---minimal-emergency-sos/beacon-android/DEVELOPER_NOTE.md)** — Personal developer note.
