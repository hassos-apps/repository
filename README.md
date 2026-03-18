# HassOS Apps Repository

> A curated ecosystem of purpose-built Home Assistant apps, crafted with structure, clarity and long-term reliability.

[![Add to Home Assistant][repository-badge]][repository-url]

## Installation

1. In Home Assistant, go to **Settings → Apps → App Store**
2. Click the menu (⋮) → **Repositories**
3. Add: `https://github.com/hassos-apps/repository`

Or click the badge above to add the repository directly.

## Available Apps

| App | Description | Version | Architectures |
|-----|-------------|---------|---------------|
| [Example](https://github.com/hassos-apps/app-example) | Example app for the HassOS Apps ecosystem | 1.0.0 | amd64, aarch64 |
| [Homebox](https://github.com/hassos-apps/app-homebox) | Inventory and organization system for the Home User | 0.24.7 | amd64, aarch64 |

## How It Works

This repository is the **app store index** for the HassOS Apps ecosystem.
Home Assistant reads the per-app directories to display metadata, documentation, icons and translations in its UI.

Each app directory is **automatically synced** via `repository_dispatch` when an app is deployed. The following files are copied from each app's source repository:

```
{slug}/
├── config.yaml          # App metadata, options and schema
├── build.yaml           # Per-architecture base images
├── DOCS.md              # User-facing documentation (shown in HA UI)
├── CHANGELOG.md         # Version history (Keep a Changelog format)
├── README.md            # App README (from repo root)
├── icon.png             # 128×128 app icon
├── logo.png             # 250×100 app logo
├── apparmor.txt         # AppArmor security profile
└── translations/
    └── en.yaml          # English UI translations
```

> **Do not edit app directories manually** — they are overwritten on every deploy.

## Security

All apps include custom AppArmor profiles, use minimal permissions and receive regular dependency updates. See `SECURITY.md` in each app for details.

---

> **[HassOS Apps](https://github.com/hassos-apps)** — purpose-built Home Assistant apps, crafted with structure, clarity and long-term reliability.

[repository-badge]: https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg
[repository-url]: https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fhassos-apps%2Frepository
