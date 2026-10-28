# BEACON Release History & Changelog

---

## [v1.0.0] - Initial Production Release (October 2026)

### Highlights & Features
- **Normal SOS**: Dedicated emergency trigger with fixed 3-second safety countdown.
- **Delayed SOS**: Timed emergency countdown (10s, 30s, 1m, 2m, 5m) for high-risk situations.
- **Offline Emergency SMS Dispatch**: Non-blocking concurrent SMS submission with carrier delivery tracking.
- **Offline Location Engine**: Concurrently queries GPS and network providers with 5-second hard deadline; generates local Google Maps coordinate links.
- **Sequential Call HUD**: Clear manual progression controls ("Call Now", "Skip", "Next Contact", "Stop Calls").
- **Tactical Follow-Up SMS**: Ability to send live situational updates to emergency contacts during an active alert.
- **Safety Test Mode**: High-contrast amber mode that simulates full dispatch without sending real SMS messages or placing calls.
- **100% Offline Autonomy**: Zero internet permissions, zero analytics, zero remote telemetry, local Room SQLite persistence only.

### Technical Artifacts
- **Package Name**: `com.beacon.sos`
- **Minimum SDK**: 26 (Android 8.0 Oreo)
- **Target SDK**: 34 (Android 14)
- **Artifact**: `app-release.apk` (~1.8 MB)
