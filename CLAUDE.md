# Instructions for Claude Code

This is CleanCut's public release repository, not its application source.

Public app updates must be built from `video_censor_desktop` using that
project's `RELEASE.md` procedure. Do not hand-edit release assets, reuse tags,
or raise `manifest.json` above `1.0.0`. The old in-place updater is retired.

Only publish a new live release when the owner explicitly requests it. Use the
signed and notarized DMG produced by:

```bash
tool/release_mac.sh
tool/sign_notarize_release.sh --publish
```
