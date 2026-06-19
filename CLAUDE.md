# Instructions for Claude Code

This is CleanCut's public release repository, not its application source.

Public app updates must be built from `video_censor_desktop` using that
project's `RELEASE.md` procedure. Do not hand-edit release assets, reuse tags,
or raise `manifest.json` above `1.0.0`. The old in-place updater is retired.

The owner has granted standing authorization to publish completed releases
after all checks in `video_censor_desktop/RELEASE.md` pass. Use the signed and
notarized DMG produced by:

```bash
tool/release_mac.sh
tool/sign_notarize_release.sh --publish
```
