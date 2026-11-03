# Beacon Release History & Changelog

---

## [v1.0.3] - Maintenance & Quality Release (November 2026)

### Highlights & Features
- **Dynamic Version Display**: Replaced static version text in Settings with dynamic build metadata generated from application configuration.
- **Real-Time Countdown Display**: Smooth, reactive ticker updates for safety countdowns across screen orientation shifts and system state restores.
- **Refined Home Screen Layout**: Streamlined the main emergency view by removing redundant static footer text.
- **Adaptive Screen Orientation**: Enabled flexible device orientation support across landscape, portrait, and foldable screens with saved navigation state.
- **Updated Application Branding**: Polished high-density app launcher icons and standardized brand text across system notifications and application UI.

### Changed
- **Home UI Streamlining**: Removed the redundant static status footer from the primary SOS screen to simplify visual layout.
- **Brand Text Standardization**: Unified application title casing to "Beacon" across UI elements, system status notifications, and documentation.
- **Adaptive Display Support**: Unlocked screen orientation support in the app manifest, allowing auto-rotation while preserving active screen state on orientation changes.

### Fixed
- **Settings Log Date Crash**: Fixed a crash in the Incident Logs and Details screens caused by an invalid date formatting pattern string.
- **Countdown Timer Stalling**: Resolved a countdown UI state issue by introducing a periodic view model ticker ensuring uninterrupted remaining time updates.

### Security and Build
- **Strict Release Signing Enforcement**: Configured external keystore property verification preventing release builds without dedicated signing credentials.
- **Dependency Locking & Verification**: Added configuration lockfiles and verification metadata to enforce reproducible build dependencies.
- **Cleartext Traffic Restriction**: Enforced `android:usesCleartextTraffic="false"` in the application manifest for enhanced security posture.
- **Modern API Compatibility**: Refactored broadcast receiver registrations and notification channel setup to use modern AndroidX compatibility bridges.

### Technical Artifacts
- **Package Name**: `com.beacon.sos`
- **Version**: 1.0.3 (`versionCode = 4`)
- **Minimum SDK**: 26 (Android 8.0 Oreo)
- **Target SDK**: 34 (Android 14)
- **Artifact**: `app-release.apk` (~1.8 MB)

---

## [v1.0.2] - Production Release (October 2026)

### Highlights & Features
- **Normal SOS**: Dedicated emergency trigger with fixed 3-second safety countdown.
- **Delayed SOS**: Timed emergency countdown (10s, 30s, 1m, 2m, 5m) for high-risk situations.
- **Offline Emergency SMS Dispatch**: Non-blocking concurrent SMS submission with carrier delivery tracking.
- **Offline Location Engine**: Concurrently queries GPS and network providers with 5-second hard deadline; generates local Google Maps coordinate links.
- **Sequential Call HUD**: Clear manual progression controls ("Call Now", "Skip", "Next Contact", "Stop Calls").
- **Follow-Up SMS**: Ability to send live situational updates to emergency contacts during an active alert.
- **Safety Test Mode**: High-contrast amber mode that simulates full dispatch without sending real SMS messages or placing calls.
- **Network-Offline Operation**: Zero internet permissions, zero analytics, zero remote telemetry, local Room SQLite persistence only.

### Technical Artifacts
- **Package Name**: `com.beacon.sos`
- **Version**: 1.0.2 (`versionCode = 3`)
- **Minimum SDK**: 26 (Android 8.0 Oreo)
- **Target SDK**: 34 (Android 14)
- **Artifact**: `app-release.apk` (~1.8 MB)
