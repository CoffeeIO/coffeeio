---
layout: post
type: "docs"
title: "Privacy Policy — Local Whisper Unlimited for Android"
desc: "Privacy policy for the Local Whisper Unlimited Android app. Speech is transcribed on the phone; no audio or text ever leaves it."
description: "Privacy policy for the Local Whisper Unlimited Android app. Speech is transcribed on the phone; no audio or text ever leaves it."
date: 2026-10-01 12:00:00 +0100
permalink: /privacy-policy-local-whisper-unlimited/
---

_Last updated: 2026-10-01_

## Summary

Local Whisper Unlimited turns your speech into text entirely on your phone. Your voice and the resulting text are never sent anywhere: not to us, not to a cloud service, not to any third party. The app has no accounts, no analytics, no ads and no tracking.

## Microphone and audio

The app records audio only while you are dictating (the mic bubble shows a waveform while it listens, and Android shows its microphone indicator). The recording is held in memory, transcribed on the phone by a speech model, and then discarded. Audio is never saved to storage and never transmitted.

## Accessibility service

The app uses Android's Accessibility Service API for one purpose: to show the mic bubble when a text field is focused in another app, and to type your dictated text into that field. To do this it looks at which field has focus and, when inserting, at that field's current text so the dictation lands at your cursor.

- Password fields are skipped; the bubble does not appear in them.
- Nothing the service sees is stored, logged to a server or transmitted.
- The service does not read screen content for any other purpose.

You can turn the service off at any time in Android Settings → Accessibility.

## What is stored on your phone

- **Dictation history** — the text of your recent dictations (up to 500), the time, the name of the app it was meant for, and the length of the recording. It lives in the app's private storage so you can recover text if inserting it fails. You can delete single entries, clear all of them, or turn history off in the app.
- **Clipboard** — each dictation is also copied to the clipboard, so you can paste it if it could not be typed into the field.
- **Settings** — your chosen model, languages, bubble options, and a count of today's dictations for the free plan.
- **Speech models** — the model files you choose to download.

All of this is removed when you uninstall the app.

## Network use

The app uses the internet only for two things:

1. **Downloading a speech model**, when you tap Download. The file is fetched from Hugging Face (huggingface.co), which, like any web server, sees your IP address. No audio, text or identifier is sent.
2. **Google Play Billing**, to offer and verify the one-time "Unlimited" purchase. Payment is handled entirely by Google Play under [Google's privacy policy](https://policies.google.com/privacy); we only learn from Play whether the purchase is owned.

## What is _not_ collected

- No audio, transcripts or typed text leave the phone.
- No analytics, telemetry, crash reporting or advertising identifiers.
- No account, name, email or contacts.
- No data is sold or shared with anyone.

## Children

The app is not directed at children and collects no personal data from anyone.

## Changes

If this policy changes, the new version will be posted on this page with a new date.

## Contact

Questions about this policy: [{{ site.email }}](mailto:{{ site.email }}).
