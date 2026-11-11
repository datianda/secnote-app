# Secnote Privacy Policy (Android)

**Effective date: November 11, 2026**　|　[中文](privacy-zh.md)

Secnote (密记本, "the app") is developed and operated by **WANWU LAB (玩物丧志软件)** ("we", "us").

**In short: the app does not request the Internet permission. It does not collect, upload or share any of your data. Your notes and passwords exist only on your own phone, encrypted with your master password.**

## 1. The app itself

- **No Internet permission.** The app does not request Android's `INTERNET` permission, so the system does not allow it to open any network connection. You can check this yourself under *Settings → Apps → Secnote → Permissions*.
- **Nothing is collected or reported.** There are no accounts, no analytics, no crash reporting, no usage statistics and no ads.
- **Notes and passwords** are stored only in the app's private storage, encrypted with your master password (Argon2id + XChaCha20-Poly1305). They never leave your device unless you export them yourself, and we have no way to read them. If you forget your master password, we cannot recover it.
- **Local preferences** (theme, auto-lock time, sort order, the start of your free trial) are kept in the app's private storage. They contain no note content and are never sent anywhere.
- **No cloud backup.** Android's automatic backup is turned off for this app. Your vault leaves the phone only when you choose *Export*.
- **Clipboard.** When you copy a password or code, it is marked as sensitive (so Android hides it in the clipboard preview) and cleared after 30 seconds.

## 2. Autofill and the Secnote keyboard

- If you choose Secnote as your **autofill service**, Android passes the app the **structure of the login form** you are looking at (which fields exist and their types, the requesting app's package name, the website's domain) so it can find matching logins in your vault. This is processed only on your phone. It is not stored, unless you choose to save a new login, and it is never sent anywhere.
- To protect you from impostor apps, the app reads the requesting app's **signing-certificate fingerprint** and, with your confirmation, records it in the matching entry.
- If you enable the **Secnote keyboard**, it only types the username, password or code you pick into the current field. It does not record anything you type.

## 3. Other features that use device capabilities

All of these are optional and work entirely on your phone:

- **Fingerprint / face unlock.** If you turn it on, your master password is encrypted with a key held in your phone's secure hardware (Android Keystore) and can only be released after biometric verification. We never receive your biometric data; Android handles it.
- **YubiKey (NFC / USB).** If you use a security key as a second factor, the app talks to it directly over NFC or USB on your phone.
- **Quick capture** (share sheet, selected text, quick-settings tile, "Save to Secnote" print option). Content you send to the app is encrypted into your vault. To accept content while the vault is locked, a delivery ticket is stored in the app's private storage, encrypted with a key in Android Keystore.
- **Notifications** are used only to tell you that a printed document is waiting to be saved.
- **Device identifier.** The app reads Android's per-app identifier (`ANDROID_ID`) only to compute a one-way fingerprint used to check offline licence files (see section 5). It never leaves the device.

## 4. Purchases (Google Play version)

- The Google Play version is free to install and includes a 14-day free trial of all features. After the trial, unlocking editing and autofill is a one-time purchase made through **Google Play Billing**. Without a purchase the app stays usable in read-only mode: you can always view, copy and export your data.
- Payment is handled by Google under the [Google Privacy Policy](https://policies.google.com/privacy). We never see your payment details.
- The app verifies Google's signed purchase receipt on your phone and keeps a copy of that receipt in its private storage, so the purchase still works when Google Play cannot be reached. Nothing is sent to us.
- The Google Play Billing library talks only to the Google Play Store app on your phone. In Secnote it has no Internet permission of its own.

## 5. Licence files (version downloaded from our website)

The version downloaded from our website or GitHub can import an offline licence file (`secnote.license`) issued by us. A licence file may contain your licence name, its expiry date and the device fingerprint described in section 3. It is checked only on your phone and is never sent back. Information you give us when buying a licence is covered by the privacy policy on our website.

## 6. Deleting your data

All data is on your phone. Uninstalling the app, clearing its storage, or deleting the vault in the app removes it. Copies you exported yourself are under your control.

## 7. Children

The app is intended for adults and is not directed at children.

## 8. Changes and contact

If this policy changes, we will publish the new version on this page and update the effective date. Questions: **mente337@outlook.com**.
