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

## Data packs
| File | Contents |
|---|---|
| `packs/rulepacks-2026.11.12.aijpack` | The 7 rule packs exactly as shipped in 0.9.0 (AMD MI355X, DGX B200, B300 Spectrum-X, B300 XDR, GB200, GB300, Vera Rubin NVL72) |

Install with `p2p datapack install rulepacks-2026.11.12.aijpack`, or POST to `/api/datapacks` (settings role). Both need app version 0.9.1 or later.
