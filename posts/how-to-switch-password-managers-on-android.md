---
title: "How to Switch Password Managers on Android Without Exporting a CSV"
seo_title: "Switch Password Managers on Android: Passkeys and Passwords"
meta_description: "Android can now move passwords and passkeys between Google Password Manager, 1Password, Bitwarden, and Dashlane without a downloaded file. Here is how the transfer works."
url_slug: how-to-switch-password-managers-on-android
primary_keyword: switch password managers Android
related_keywords:
  - transfer passkeys Android
  - Google Password Manager import
  - Credential Exchange Android
  - 1Password Bitwarden Dashlane Android
  - move passwords without CSV
category: Android Apps & Updates
tags:
  - Android
  - Password managers
  - Passkeys
  - Google Password Manager
date: 2026-09-14
featured_image_prompt: "Editorial technology photograph of a modern Android phone on a wooden desk next to a simple hardware security key and a closed notebook, soft natural light, no readable UI text or brand logos, clean magazine style, photorealistic."
---

# How to Switch Password Managers on Android Without Exporting a CSV

Moving a password vault used to mean downloading a spreadsheet of every login you own. That file sat unencrypted on the phone until you remembered to delete it. Passkeys were worse: many managers could not export them at all, so you had to recreate each one site by site.

On September 10, 2026, Google announced a built-in Android transfer that moves passwords and passkeys between supported managers in a few taps. The phone coordinates the handoff. You never download a CSV.

This guide covers what the feature does, which apps support it today, and the exact path to start a transfer.

## What changed

Google’s Android blog describes three problems the old workflow created:

- Password exports were often plain-text files.
- Passkeys could not move with the rest of the vault.
- Switching tools felt permanent because the cleanup work was painful.

The new flow uses Android as a broker. Your destination manager asks the system to import. Android lists compatible managers already installed on the device. You review and approve the move inside the source app. The data crosses between apps in a few seconds.

Google says the experience works on Android 8 and later.

This is the consumer face of a broader Credential Exchange effort. Android developer documentation already points partners at a credential-transfer API so more apps can join the same path.

## Which password managers support it

As of Google’s September 10 announcement, the transfer works with:

- Google Password Manager
- 1Password
- Bitwarden Password Manager
- Dashlane

Google says more partners will follow. If the manager you want is missing from the import picker, it has not implemented the Android handoff yet. Do not assume every vault app on your home screen is eligible.

You still need both apps installed on the same phone for this method. The system detects local managers; it is not a cloud-to-cloud move that you start from a website.

## Before you start

Do a short checklist so you are not debugging mid-transfer.

- Update Android System WebView and Google Play services from the Play Store.
- Update both the source and destination password manager apps.
- Unlock the source vault once so you are already signed in.
- Confirm the destination account is the one you want to keep long term.
- Stay on Wi-Fi if the destination manager also syncs to its own cloud after the local copy lands.

If you use a work profile, run the transfer from the profile that actually holds the vault. Personal and work copies of the same app do not always see each other.

## How to import into a new manager

Google’s published steps are destination-first. You start in the app you want to use going forward.

1. Open the **new** password manager (for example, 1Password, Bitwarden, Dashlane, or Google Password Manager).
2. Look for **Import**, **Copy from another provider**, or a similar settings item. Wording varies by app; the important part is that the app hands the job to Android instead of asking for a file.
3. When Android takes over, it lists password managers it can import from on this device.
4. Choose the **old** manager and tap **Continue**.
5. Android opens the source app so you can review what will move and authorize the transfer.
6. Approve the request. Wait for the confirmation that passwords and passkeys finished copying.

Google Password Manager also advertises the reverse: exporting out of Google is the same coordinated path, not a manual file dump.

For Google-specific screens, Google points to its Help Center article on importing passwords and passkeys on Android (`support.google.com/chrome` credential exchange topic).

### What you should see if it worked

- Passwords appear in the destination vault with site, username, and secret intact.
- Passkeys that the source manager stored locally appear as passkeys, not as leftover password rows.
- You can sign in to a test site with a passkey from the new manager after you set that manager as an autofill or passkey provider.

If passkeys are missing, the source app may not have stored them, or that item may still live only on another device. The Android transfer moves what is on the phone’s participating manager, not every credential in a desktop-only vault.

## Set the new app as your autofill provider

Copying the vault is only half the switch. Android still fills logins from whichever service is selected in Settings.

On most phones:

1. Open **Settings**.
2. Search for **Autofill service**, **Preferred service**, or **Passwords, passkeys and autofill** (Pixel wording varies by version).
3. Select the manager you just imported into.
4. Open that manager’s settings and confirm Autofill / passkeys are on.
5. Lock the phone, reopen a login page, and confirm the new app offers the credential.

On Android 14 and later, Credential Manager can surface passkeys from more than one enabled provider. Even so, pick a primary manager so you are not maintaining two live vaults by accident.

## After the transfer

Treat the old vault as a backup until you have signed into the accounts you use every week.

- Test email, banking, work SSO, and one passkey-only site.
- Turn on the destination manager’s own sync and two-factor protection.
- When you are confident, stop saving new logins to the old app.
- Uninstall the old manager only after its cloud copy is something you still control or have deliberately deleted.

Do not leave two managers offering the same password. You will update one copy and wonder why a site still has the old secret.

## What this does not replace

The Android handoff is safer than a CSV sitting in Downloads. It is not a substitute for account hygiene.

- It does not rotate reused passwords. If ten sites share one secret, they still share it after the copy.
- It does not move 2FA authenticator codes unless that is a separate feature in the destination app.
- It does not fix a manager that never stored a passkey in the first place.
- Availability still depends on both vendors shipping the Android transfer, not only on Google announcing the platform.

If a manager is absent from Google’s partner list, keep using that vendor’s official export until it joins. A CSV is still better than losing the vault, but delete the file from the device and from any cloud folder as soon as the import finishes.

## A practical example

Suppose Bitwarden has been on the phone for years and you want 1Password.

Install and sign in to 1Password. Start its import-from-another-provider action. Android should offer Bitwarden. Approve the request inside Bitwarden. When the copy completes, set 1Password as the autofill service. Sign in to two or three real sites. Only then pause Bitwarden autofill.

The same pattern works toward Google Password Manager if you want logins tied to your Google Account, or away from Google if you want a third-party vault as the source of truth.

## Conclusion

Android can now move passwords and passkeys between Google Password Manager, 1Password, Bitwarden, and Dashlane without leaving an exported file on the device. Start in the destination app, let Android list compatible sources, review the request in the old manager, then switch autofill.

If the import option never appears, update both apps and Play services, confirm you are on Android 8 or later, and check that both products are on Google’s current partner list. Switching tools should be a settings task, not a weekend of recreating passkeys.

## Sources

- Google: [Switching password managers is easy and safe on Android](https://blog.google/products-and-platforms/platforms/android/switch-password-managers/)
- Android Developers: [Credential transfer](https://developer.android.com/identity/sign-in/credential-transfer)
- Google Help: [Import passwords and passkeys on Android](https://support.google.com/chrome?p=credential_exchange_android)
- Google Developers: [Passkey support on Android and Chrome](https://developers.google.com/identity/passkeys/supported-environments)
