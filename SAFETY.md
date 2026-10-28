# BEACON Safety, Limitations & Testing Guidance

> [!IMPORTANT]
> Please read this document carefully to understand the operation, platform capabilities, and physical limitations of BEACON before relying on it in real-world scenarios.

---

## 1. Physical & Hardware Requirements

1. **Active Cellular Network Connection**:
   - Outbound SMS messages and voice calls require an active SIM card and adequate cellular signal coverage from your mobile carrier.
   - If Airplane Mode is enabled or cellular service is unavailable, outbound alerts will fail. BEACON displays clear failure statuses and retry options when network service returns.
2. **Device Power & Battery**:
   - BEACON utilizes background foreground service execution with partial WakeLocks during active emergency activations to prevent system sleep. However, an active battery is required.

---

## 2. Android OS Platform Limitations

Under official Android security policies:
1. **Third-Party Call Answer Detection**:
   - Android operating system APIs **do not** inform third-party applications whether a phone call was answered by a human, answered by voicemail, or rang out.
   - The OS `TelephonyManager` only reports call state transitions (`CALL_STATE_OFFHOOK`, `CALL_STATE_IDLE`).
   - **BEACON does not make false promises that a call was answered.** Instead, BEACON provides clear manual call HUD controls ("Call Now", "Skip", "Next Contact", "Stop Calls") so you can manage contact progression reliably.

2. **Location Fix Timestamps**:
   - Emergency SMS messages report exact fix age (e.g., `(LAST KNOWN 14m ago, ±15m)` or `LIVE`).
   - Coordinates are generated directly from local GPS hardware and are **never fabricated**. If GPS is unavailable or disabled, the message explicitly states `[Location coordinates unavailable offline]`.

---

## 3. Safe Testing Guidance

> [!CAUTION]
> **DO NOT TEST BEACON AGAINST REAL EMERGENCY SERVICES (911, 112, 999, ETC.).**
> Calling public emergency dispatchers when there is no genuine emergency is illegal and places real lives at risk.

### How to Safely Test BEACON
1. **Use Safety Test Mode**:
   - Toggle **Safety Test Mode** in BEACON settings.
   - The UI switches to high-contrast amber.
   - In Safety Test Mode, all cellular SMS transmissions and phone calls are completely bypassed and simulated locally.
2. **Testing with Consenting Personal Contacts**:
   - Turn off Safety Test Mode only when testing with designated personal friends or family members who have explicitly agreed to receive test messages and calls.
   - Always notify your contacts in advance before triggering a live test alert.
