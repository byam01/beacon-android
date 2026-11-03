# Beacon Privacy Policy & Data Disclosure

**Effective Date**: November 2026  
**Last Updated**: November 2026

Beacon is engineered around complete data transparency, minimal permission usage, and local user control.

---

## 1. Network Disconnection & Zero External Data Collection

- **No Internet Permission**: Beacon's manifest explicitly **does not request** the `android.permission.INTERNET` permission. The application cannot transmit IP network data to any remote server or endpoint.
- **No Developer Backend**: Beacon operates without cloud servers, user accounts, remote databases, or external APIs.
- **No Analytics or Telemetry**: Beacon includes zero analytics frameworks, zero crash-reporting SDKs, zero advertising libraries, and zero third-party tracking scripts.
- **Zero Third-Party Sharing**: No user data, contact information, location coordinates, or usage logs are collected or sold by the developer or shared with third parties.

---

## 2. On-Device Local Data Storage

All application configuration and history—including emergency contacts, custom SMS template text, timer settings, and emergency dispatch logs—is stored exclusively on your device using Android's Room persistence library (SQLite).

- **Storage Location**: Data is stored inside Android's app-private data directory (`/data/data/com.beacon.sos/databases/`), protected by standard Android OS sandboxing security.
- **Data Lifecycle**: Uninstalling Beacon completely purges all local app database files and configuration preferences from your device.

---

## 3. Cellular Telephony & Android Runtime Permissions

Beacon requests runtime Android permissions strictly to execute emergency alerting features directly initiated by the user:

| Permission | Purpose in Beacon | Transmission Scope |
| :--- | :--- | :--- |
| `SEND_SMS` | Transmits emergency SMS alerts to user-designated contacts upon activation | Outbound SMS sent via your cellular carrier to designated contacts only |
| `CALL_PHONE` | Initiates voice phone calls to designated emergency contacts | Outbound phone calls handled by your device's cellular telephony subsystem |
| `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` | Queries local GPS/network providers to append current location coordinates / Google Maps link to outbound SMS | Included inside outbound SMS messages sent to designated contacts |
| `READ_CONTACTS` | Allows selecting emergency contacts directly from your device address book | Kept local within the app's local database |
| `POST_NOTIFICATIONS` | Displays active emergency status, safety countdowns, and call controls | Displayed locally on device lock screen and notification shade |

---

## 4. Contact & Support

For questions or inquiries regarding privacy and data handling in Beacon, please review this public policy or refer to the release notices in this repository.
