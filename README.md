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
- The container runs as `nobody:users` (`--user 99:100`). Create the appdata
  folder with that owner before first start:
  `mkdir -p /mnt/user/appdata/unkeep && chown 99:100 /mnt/user/appdata/unkeep`.
- Full settings: [UnKeep self-hosting guide](https://github.com/BrettKinny/UnKeep/blob/main/docs/self-hosting.md#unraid-settings).
