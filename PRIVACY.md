# BEACON Privacy Policy & Data Disclosure

**Effective Date**: October 2026  
**Last Updated**: October 2026

BEACON is designed from the ground up to respect absolute user privacy and data sovereignty.

---

## 1. Zero Network Transmission & 100% Offline Autonomy

- **No Internet Permission**: BEACON's manifest explicitly **does not request** the `android.permission.INTERNET` permission.
- **No Remote Servers**: BEACON has no backend servers, cloud databases, or API integrations.
- **No Tracking / Analytics**: Zero crash reporting SDKs, zero user tracking libraries, zero advertising frameworks, and zero third-party telemetry.
- **Zero Data Collection**: BEACON never collects, transmits, sells, or shares personal data with any third party.

---

## 2. On-Device Storage (Room SQLite)

All application state—including designated emergency contacts, custom SMS template texts, delayed timer settings, and emergency activation logs—is stored exclusively on your device in an encrypted local SQLite database via Android's Room persistence library.
- Data remains strictly on your device.
- Uninstalling BEACON completely purges all local app data.

---

## 3. Android Runtime Permissions Usage

BEACON requests runtime permissions solely to perform emergency alerts initiated directly by the user:

| Permission | Purpose in BEACON | Data Destination |
| :--- | :--- | :--- |
| `SEND_SMS` | Transmits emergency SMS alerts to user-selected contacts upon activation | Outbound SMS via cellular carrier to selected contacts only |
| `CALL_PHONE` | Initiates voice phone calls to designated emergency contacts | Outbound phone calls via device telephony subsystem |
| `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` | Appends current GPS coordinates / Google Maps link to emergency SMS | Included inside outbound SMS sent to selected contacts |
| `READ_CONTACTS` | Allows user to pick emergency contacts directly from phonebook | Kept local inside device database |
| `POST_NOTIFICATIONS` | Displays active emergency status, countdowns, and call controls | Displayed locally on device lock screen / notification shade |

---

## 4. Contact & Support

For privacy inquiries regarding BEACON, please review this public policy or refer to official release notices in this repository.
