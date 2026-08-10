# Install Boooply Mail on macOS

Boooply Mail is an invitation-only beta. You need an invitation and an active
account before you can sign in.

The app is ad-hoc signed and is not notarized by Apple, so macOS may block the
first launch. Do not disable Gatekeeper globally.

## 1. Download the correct installer

Check **Apple menu → About This Mac**:

- Apple M-series chip: download the `arm64` DMG.
- Intel processor: download the `x64` DMG.

Download the DMG and `SHA256SUMS` from the same
[official Release](../../../releases), then follow the
[verification guide](verify-checksums.md). Continue only when the DMG reports
`OK`.

## 2. Install the app

1. Open the verified DMG.
2. Copy **Boooply Mail** to **Applications**.
3. Eject the disk image.
4. Open Boooply Mail once.

## 3. Approve the first launch

If macOS blocks the app:

1. Open **System Settings → Privacy & Security**.
2. Find the message for Boooply Mail.
3. Click **Open Anyway**.
4. Authenticate and confirm the launch.

This approves only Boooply Mail. Never disable Gatekeeper globally or remove
quarantine attributes from arbitrary downloads.

## 4. Sign in

Complete the invitation flow, then sign in with the invited account. Do not
share the invitation link.

Invited testers may report non-sensitive problems through
[Issues](../../../issues). Follow the [security policy](../SECURITY.md) for
anything sensitive.

## Update or roll back

The beta does not update automatically. To change versions:

1. Download the desired DMG and its `SHA256SUMS` file.
2. Verify the DMG.
3. Quit Boooply Mail.
4. Replace the app in **Applications**.

Do not delete application data or macOS Keychain entries during a normal
update or rollback.
