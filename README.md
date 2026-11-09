# Void Runner: Signal Break — Official Update Distribution

This **public repository** hosts only approved release packages and update
manifests for Void Runner: Signal Break by BlackTop Interactive.

The game's development repository and source code remain private.

## Distribution layout

- GitHub Releases: immutable, versioned signed Windows installers and their `.sig` files.
- `stable/latest.json`: stable signed update manifest.
- `beta/latest.json`: beta signed update manifest.

**No update manifest has been published yet.** The channels will become live
only after the first signed build is approved and verified.

The application uses Tauri's signature verification to validate updates.
A release ZIP or source tree is not required for players to use the in-game
**Check for Updates** → **Update & Restart** flow.

## Release safety rules

1. Never commit or upload a signing **private** key, release build credentials,
   internal source code, or player save databases.
2. The signing key remains on the owner's build machine and offline backup.
3. Versioned GitHub Release binaries must exist and be downloadable **before**
   advancing a channel's `latest.json` manifest.
4. Releases are explicitly approved and signed by the owner. No automatic
   GitHub-to-player installation occurs without a signed approved package.
5. Stable and beta are separate channels, with versioned release tags such as
   `v0.1.3` and `v0.1.3-beta`.

## Development

For the private game source, release tooling, and player-save compatibility
requirements, use the internal BlackTop Saga source repository.
