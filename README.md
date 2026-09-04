# Hubble for macOS

This public repository contains the official signed Hubble and HubDash downloads and their
automatic-update feeds. The application source remains in a private repository; no source code,
signing credentials, or GitHub access tokens are shipped here or embedded in the apps.

## Install

Hubble currently supports Apple Silicon Macs running macOS 13 or later.

1. Open the [latest Hubble release](https://github.com/Lightlab24/Hubble-Releases/releases/latest).
2. Download `Hubble-X.Y.Z.pkg` and open it.
3. Follow the macOS installer. It installs both `/Applications/Hubble.app` and
   `/Applications/HubDash.app`.
4. Open Hubble, then open HubDash from Hubble's menu when you need the dashboard.

The release also includes a DMG for manual installation. If you use it, drag both Hubble and
HubDash into the Applications folder.

All releases are Developer ID signed and notarized by Apple. `SHA256SUMS` is included with every
release for an independent download-integrity check.

## Updates

Hubble checks the public update feed when it starts and every 30 minutes while it is running. You
can also choose **Check for Updates…** from Hubble at any time. When an update is available,
HubDash shows an **Update** button and asks whether to install it. Choosing **Not now** keeps the
button available and suppresses the automatic prompt until Hubble is reopened.

An accepted update downloads the signed package, asks for macOS authorization when required,
replaces Hubble and HubDash together, and relaunches them. The updater reads only these public
files:

- [`latest.json`](https://raw.githubusercontent.com/Lightlab24/Hubble-Releases/main/latest.json)
- [`appcast.xml`](https://raw.githubusercontent.com/Lightlab24/Hubble-Releases/main/appcast.xml)

## Release contents

Each GitHub release contains the notarized PKG and DMG, the two update-feed documents, and
`SHA256SUMS`. Report an installation or update problem through the project's normal support
channel and include the Hubble version and the exact macOS error message.
