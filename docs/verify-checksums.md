# Verify a Boooply Mail download

Every macOS release includes a `SHA256SUMS` file. Download it from the same
release as the DMG you want to install.

Open Terminal and move to the folder containing both files.

For Apple Silicon, set the downloaded filename:

```bash
DMG="Boooply-Mail-0.1.0-mac-arm64.dmg"
```

For Intel, use:

```bash
DMG="Boooply-Mail-0.1.0-mac-x64.dmg"
```

Replace `0.1.0` with the downloaded version, then run:

```bash
awk -v file="$DMG" '$2 == file { print }' SHA256SUMS | shasum -a 256 -c -
```

The result must show the exact DMG filename followed by:

```text
OK
```

Do not install the DMG if verification fails, finds no matching checksum, or
the files came from different releases. Download both files again from the
[official Releases page](../../../releases).

If a fresh download still fails, open a non-sensitive issue with the release
version, Mac architecture, and exact error message. Do not attach credentials
or private application data.
