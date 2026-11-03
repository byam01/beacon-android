# Beacon Safety, Limitations & Testing Guidance

> [!IMPORTANT]
> Please read this document carefully to understand the operation, platform capabilities, and physical limitations of Beacon before relying on it in real-world scenarios.

---

## 1. Physical & Hardware Requirements

1. **Active Cellular Network Coverage**:
   - Outbound emergency SMS messages and voice phone calls require an active SIM card and cellular network signal coverage from your mobile carrier.
   - If Airplane Mode is active, SIM card is missing, or cellular coverage is unavailable, outbound cellular alerts cannot be transmitted. Beacon displays clear error indicators and retry controls when network signal returns.
2. **Device Battery & Background Execution**:
   - Beacon utilizes background foreground service execution with partial CPU WakeLocks during active emergency activations to prevent system sleep. Active battery power is required.

---

## 2. Android OS Platform Limitations

Under official Android security policies:
1. **Call Answer Detection**:
   - Android operating system APIs **do not** inform non-dialer applications whether a phone call was answered by a human, answered by voicemail, or rang out without answer.
   - Android's `TelephonyManager` only reports call state transitions (`CALL_STATE_OFFHOOK`, `CALL_STATE_IDLE`).
   - **Beacon does not claim that a recipient answered a call.** Instead, Beacon provides clear manual call HUD controls ("Call Now", "Skip", "Next Contact", "Stop Calls") so you can manage contact progression reliably.

2. **Location Accuracy & Timestamps**:
   - Emergency SMS messages report coordinates directly from local hardware providers (`GPS_PROVIDER` / `NETWORK_PROVIDER`) with explicit fix age and accuracy metadata (e.g., `LAST KNOWN 14m ago, ±15m` or `LIVE`).
   - Coordinates are reported directly from device location providers without artificial estimation. If location services are disabled or fail to return a fix within the 5-second deadline, the message states `[Location coordinates unavailable offline]`.

---

## 3. Safe Testing Guidance

> [!CAUTION]
> **DO NOT TEST BEACON AGAINST REAL EMERGENCY SERVICES (E.G., 911, 112, 999).**
> Placing test calls to public emergency dispatchers when there is no genuine emergency is illegal and risks lives.

### How to Safely Test Beacon
1. **Use Safety Test Mode**:
   - Toggle **Safety Test Mode** in Beacon settings.
   - The UI switches to high-contrast amber.
   - In Safety Test Mode, all cellular SMS transmissions and phone calls are completely bypassed and simulated locally.
2. **Testing with Consenting Personal Contacts**:
   - Turn off Safety Test Mode only when testing with designated personal friends or family members who have explicitly agreed to receive test messages and calls.
   - Always notify your contacts in advance before triggering a live test alert.
