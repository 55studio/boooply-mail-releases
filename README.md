# Boooply Mail — Public Beta Releases

This repository provides official public-beta downloads, checksums, release
notes, and installation instructions for Boooply Mail.

The application source code is maintained separately and is not published in
this repository.

## Current availability

No public beta has been published yet.

When a tested beta is ready, installers will be available from the
[Releases](../../releases) page.

## Supported platforms

The first public beta is planned for:

- macOS on Apple Silicon
- macOS on Intel

Windows support is planned separately and will not be inferred from the macOS
builds.

## Important macOS security notice

The initial macOS public beta will be ad-hoc signed. It will not be signed with
an Apple Developer ID and will not be notarized by Apple.

Because of this, macOS may prevent the application from opening normally after
download. The release instructions will explain how to use the per-application
**Open Anyway** option in macOS System Settings.

You should never disable Gatekeeper globally.

Only download Boooply Mail from the Releases page of this official repository.

## Verifying a download

Each release will include:

- An installer for Apple Silicon
- An installer for Intel Macs
- A `SHA256SUMS.txt` checksum file
- A release manifest describing the source revision and build

Before installing, download the checksum file and verify the installer:

```bash
shasum -a 256 -c SHA256SUMS.txt
