---
layout: default
title: HomeRun — Privacy Policy
---

# Privacy Policy — HomeRun

**Effective date:** May 27, 2026
**Developer:** fraivor-ai
**Contact:** fraivor@gmail.com

---

## The Short Version

HomeRun stores everything on your device and nowhere else. The only time any information leaves your phone is when an absence is detected — at that point, a message is sent directly to the successor(s) you configured. The developer has zero access to your data, ever.

---

## 1. Information We Collect

HomeRun does not collect information about you. All data you enter — vault items, your phone PIN, your legal authorization, your emergency contacts — is encrypted on your device and never transmitted to any server operated by the developer.

The information stored locally on your device includes:

- **Vault items**: documents, notes, account credentials, and file attachments you add to your heritage vault
- **Emergency contacts**: names and contact details of your designated successors
- **Phone access information**: your device PIN code and master password hint
- **Legal consent and digital signature**: your signed authorization document
- **Activity data**: timestamps of app activity used to detect absence
- **Subscription status and ad credits**: your tier (Basic or Premium) and earned ad credit balance

All of the above is encrypted with AES-256 and stored exclusively on your device using the operating system's secure storage (iOS Keychain / Android Keystore).

---

## 2. How Your Information Is Used

Your data is used only to operate the app on your behalf:

- Activity timestamps determine whether an absence threshold has been reached
- Vault contents are displayed to you (the owner) within the app
- The phone PIN and master password hint are included in the absence notification sent to your successor

The developer cannot access any of this information. There is no backend server, no database, no analytics, and no crash reporting that uploads personal data.

---

## 3. When Information Is Transmitted

HomeRun transmits data in exactly two situations:

### 3a. Absence Notifications

When your configured absence threshold is reached, the app sends a notification to each successor you designated. **How this works differs by platform:**

**Android:**
Notifications are sent as SMS messages directly from your device using Android's native `SmsManager`. No third-party messaging service is involved — the message travels peer-to-peer from your phone number to your successor's phone number, the same as a regular text message you would send yourself.

**iOS:**
Apple does not permit apps to send SMS messages silently in the background. On iOS, the app opens the Messages app with the notification pre-filled so you can review and send it manually. For fully automatic absence notifications on iOS (so alerts go out even if you are unreachable), you must configure your own **Brevo** (brevo.com) email account in the app's settings. Absence emails are then sent through your Brevo account to your successor's email address.

The notification (whether SMS or email) contains:

- Your phone PIN code
- Your master password hint
- Device location notes you entered during setup
- Instructions for your successor to access your vault

The developer does not receive a copy of these messages.

### 3b. Brevo Email (iOS and optional Android)

If you configure Brevo for email alerts, the absence notification email is sent via **your own Brevo API key**, which you provide and which is stored only on your device. Brevo processes the email in transit per their [Privacy Policy](https://www.brevo.com/legal/privacypolicy/). The developer has no access to your Brevo account or the emails sent through it.

### 3c. In-App Purchases

If you purchase the Premium plan, the payment is processed entirely by Apple (App Store) or Google (Google Play). HomeRun never sees your payment card or billing details. Purchase receipts are verified locally on your device.

---

## 4. Third-Party SDKs

### Google AdMob (Basic tier only)

If you use the Basic tier, the app shows rewarded video ads via **Google AdMob**. AdMob may collect your device's advertising identifier (IDFA/GAID), IP address, and ad interaction data to serve and measure ads. This is governed by [Google's Privacy Policy](https://policies.google.com/privacy). You can opt out of personalized ads through your device's advertising settings.

Premium users do not see ads and AdMob is not active for their sessions.

### AppLovin MAX (Basic tier, post-launch)

HomeRun includes the AppLovin MAX SDK as an ad mediation layer. It is currently **disabled** and will only become active after a future app update. When enabled, it will be subject to [AppLovin's Privacy Policy](https://www.applovin.com/privacy/). You will be notified in the app's release notes before it activates.

### Apple App Store / Google Play (purchases)

In-app purchases are handled natively by Apple and Google. Their privacy policies apply to any payment information you provide during checkout.

---

## 5. Data Retention and Migration

### App Upgrades
Your encrypted data is preserved across app updates. Installing a new version of HomeRun does not erase your vault, contacts, or settings.

### Phone Migration
Your data can be migrated when you move to a new phone **within the same operating system**:

- **iOS → iOS**: Data in the iOS Keychain is included in encrypted iCloud Backup and iPhone-to-iPhone transfers via the Migration Assistant. Restoring from an iCloud or local backup to a new iPhone restores your HomeRun data.
- **Android → Android**: Data stored in Android's EncryptedSharedPreferences is included in Google Backup on supported devices. Restoring to a new Android device from a Google Backup restores your HomeRun data.

**Cross-platform migration (iOS → Android or Android → iOS) is not supported.** The encryption and secure storage layers are platform-specific and cannot be transferred between operating systems.

### Temporary Removal
If you need to temporarily uninstall HomeRun (for example, to free storage space), the app provides a **"Pause & Reinstall"** option in Settings. Activating this option pauses the absence detection timer so your successors are not alerted while you are reinstalling. After reinstalling and restoring from a backup, your data and the paused timer are restored.

If you uninstall without using the Pause option, your data may still be recoverable on iOS (Keychain items persist after uninstall by default) or on Android (if Google Backup is enabled). However, the absence timer will resume from where it left off once you reinstall.

### Successor Access
Your vault data remains on your device at all times and is only accessible through the HomeRun app. A successor can read your vault only after:

1. Physically obtaining your device
2. Unlocking it with the PIN delivered in the absence notification
3. Opening HomeRun and completing the in-app unlock payment (if applicable)

No one — including the developer, Apple, or Google — can read your vault data without completing these steps.

---

## 6. Children's Privacy

HomeRun is intended for adults managing their personal estate and digital assets. It is not directed at children under 13 (US) or 16 (EU/UK). We do not knowingly collect information from minors.

---

## 7. Data Security

- All vault data is encrypted with AES-256 before being written to disk
- PIN and credential data is stored exclusively in the device's secure enclave (iOS Keychain / Android Keystore with hardware-backed encryption)
- No data is transmitted over the internet except the absence notification described in Sections 3a and 3b
- The Brevo API key you provide is stored in the device's secure storage and is never logged or sent to the developer

---

## 8. Your Rights

Because HomeRun stores your data only on your device, you have complete control:

- **Access**: Open the app to see all stored data
- **Correction**: Edit any vault item, contact, or setting at any time
- **Deletion**: Settings → Delete All Data removes everything permanently
- **Revocation**: Settings → PIN Sync → Revoke Consent stops silent PIN monitoring and removes the stored PIN

If you have questions about personal data related to ad serving (AdMob), contact Google directly via their privacy tools at [myaccount.google.com](https://myaccount.google.com).

---

## 9. Changes to This Policy

If this policy changes in a material way (e.g., if new data collection is introduced), the updated policy will be published here and the effective date will be updated. Continued use of the app after a change constitutes acceptance.

---

## 10. Contact

For any privacy questions:

**Email:** fraivor@gmail.com
**App:** HomeRun — Passive Life-Signal Check-In & Automated Digital Inheritance App
**Developer:** fraivor-ai

---

*This policy applies to HomeRun for iOS and Android.*
