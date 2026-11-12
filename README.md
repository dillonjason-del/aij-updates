# AI INFRAJourney updates

The public download location for AI INFRAJourney by AI INFRAVeyra. The source code is private; this repository holds only:

- `update.json`: the signed update feed the app reads in Help > Check for updates.
- `downloads/`: installers (with `SHA256SUMS`). `packs/`: signed data packs.

## How it is protected
- `update.json` and every `.aijpack` data pack are signed with AI INFRAVeyra's Ed25519 key. The app holds only the public key, so it refuses any changed or forged file.
- The feed carries each installer's SHA-256 and size.
- An installer needs an AI INFRAJourney license key to run.

## Feed address
Set this in Help > Update feed, or with `P2P_UPDATE_URL`:

```
https://raw.githubusercontent.com/dillonjason-del/aij-updates/main/update.json
```
