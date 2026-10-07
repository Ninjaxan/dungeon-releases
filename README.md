# Dungeon Games Releases

Official downloads for Dungeon desktop applications. The download page with the current version,
checksum and signer is **https://dungeon.games/launcher** — start there.

## Dungeon Launcher

Every Dungeon game and world in one library, with a built-in wallet for 18 networks. Windows 10/11, 64-bit.
A signed and notarized macOS build will be published to the same release when ready.

Each release contains:

| File | What it is |
|---|---|
| `Dungeon-Launcher-Setup-<version>.exe` | The Windows installer. Code-signed as **Lee Berman** and timestamped by Microsoft. |
| `Dungeon-Launcher-Setup-<version>.exe.blockmap` | Delta-update data used by the launcher's auto-updater. Not for people. |
| `beta.yml` / `latest.yml` | The auto-update feed the installed launcher reads (beta or stable channel). |
| `launcher-provenance.json` | Version, source commit, signer, SHA-256/SHA-512 of the installer, and which packaged tests passed. |

### Verify a download

```powershell
Get-FileHash .\Dungeon-Launcher-Setup-<version>.exe -Algorithm SHA256
```

Compare with `installer.sha256` in that release's `launcher-provenance.json`. Right-click the installer →
Properties → Digital Signatures should show **Lee Berman** with a Microsoft timestamp.

Releases marked **Pre-release** are the beta channel. Version 2.x releases are the previous application and are
kept for history only.

Problems: https://discord.gg/DWKX7Y6Dtx
