# Verify a download

Download your DMG and `SHA256SUMS` from the same
[Boooply Mail release](../../../releases), then place both files in the same
folder.

Open Terminal in that folder and set the exact downloaded filename.

Apple Silicon:

```bash
DMG="Boooply-Mail-0.1.0-mac-arm64.dmg"
```

Intel:

```bash
DMG="Boooply-Mail-0.1.0-mac-x64.dmg"
```

Replace `0.1.0` with your downloaded version, then run:

```bash
awk -v file="$DMG" '$2 == file { print }' SHA256SUMS | shasum -a 256 -c -
```

Install the DMG only when the result shows its exact filename followed by
`OK`. If it fails, download both files again and do not install that copy.
