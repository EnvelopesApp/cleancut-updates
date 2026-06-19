# CleanCut Releases

This public repository hosts CleanCut's signed macOS releases.

## Current release

- App: `1.0.38`
- Engine: `1.12.5`
- Asset: `CleanCut.dmg`
- Platform: Apple Silicon, macOS 14 or later
- Stable URL:
  <https://github.com/EnvelopesApp/cleancut-updates/releases/latest/download/CleanCut.dmg>

The current app queries the GitHub Releases API on launch. When the latest tag
is newer than the installed version, it offers the customer the complete signed
and notarized DMG. CleanCut never patches its own installed bundle.

## Publishing

Publishing is driven from the private/local app source:

```bash
cd ~/Developer/video_censor_desktop
tool/release_mac.sh
tool/sign_notarize_release.sh --publish
```

The second script creates or updates the versioned `vX.Y.Z` release, uploads
`CleanCut.dmg`, and marks that release latest. The website uses the stable URL
above, so no website edit is required for a normal app update.

Never reuse a tag for a different version. Verify the release asset's size and
SHA-256 after publishing.

## Retired updater

Files from the old shell/engine chunk updater remain only for release history.
`manifest.json` is intentionally pinned to `1.0.0` with no payloads so old
clients cannot mutate their signed app bundles.

Do not bump the manifest or restore the old in-place update flow.
