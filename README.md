# Unraid templates

Unraid Community Applications templates maintained by Brett Kinny.

| App | Template | Image |
| --- | --- | --- |
| [UnKeep](https://github.com/BrettKinny/UnKeep) | [`templates/unkeep.xml`](templates/unkeep.xml) | `ghcr.io/brettkinny/unkeep` |

Report problems with an app on that app's GitHub issues page. Use this
repository's issues only for problems with the template itself.

## UnKeep notes

- **HTTPS is required.** Browsers block the encryption UnKeep uses on plain-HTTP
  addresses, so publish it through Tailscale Serve, a reverse proxy, or
  Cloudflare Tunnel.
- The relay runs as `nobody:users` (`PUID=99`, `PGID=100`). It starts as root
  only long enough to give its appdata folder to that user, so the folder needs
  no manual `chown`, then drops all privileges.
- Full settings: [UnKeep self-hosting guide](https://github.com/BrettKinny/UnKeep/blob/main/docs/self-hosting.md#unraid-settings).
