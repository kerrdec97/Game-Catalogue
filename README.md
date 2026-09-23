# Game Catalogue

A Windows desktop app for browsing game libraries from DLPS, SUPERPSX, PFS/LZ4/FPKG, and exFAT sources.

Fetches each source's catalogue, normalizes its releases and download links, and presents them with cover art, title IDs, source-aware filters, and variant details.

The application is distributed as a closed-source Windows executable.

---

## Features

- Keeps four source libraries isolated in their own tabs and datasets
- Ships as a standalone Windows executable with its own Node.js runtime
- Decodes the live PFS catalog's Base64 download URLs
- Decrypts exFAT source links locally
- Parses Backport / Standard / DLC / Fix builds per post
- Source-specific, combinable platform/format/content/firmware filters
- One card per game with merged PFS, LZ4, FPKG, DLC, and backport variants
- Optional separate cards for PFS, LZ4, and FPKG releases
- Expanded search across title IDs, releases, firmware, credits, and hosts
- Per-source refresh with partial-refresh protection and automatic backups
- Persistent favourites, theme, page size, and filter selections
- Working light and dark themes plus per-source JSON export
- Progressive View All rendering for large libraries
- Numbered pages return the game grid to the top; View All keeps your place while loading more
- Source health and application-data access in Settings

---

## Download

Download the latest Windows build from [Releases](https://github.com/kerrdec97/Game-Catalogue/releases). The ZIP package is recommended because it includes the application and its accompanying legal notices.

### v0.0.4 pagination update

- Changing numbered results pages now starts at the top of the new page in every catalogue tab.
- View All's Load More action retains your scroll position.

See the [v0.0.4 release notes](https://github.com/kerrdec97/Game-Catalogue/releases/tag/v0.0.4).

### v0.0.3 maintenance update

- Improved exFAT cover delivery and image-format compatibility, including existing saved libraries.
- Added alternate image delivery when a cover request fails.
- Removed the DLPS scraper's mandatory full crawl of the auxiliary DownloadGamePS3 site. Unavailable auxiliary pages retain their original links.
- Failed or blocked DLPS pages now stop the refresh without replacing the saved catalogue and report an actionable error.

**DLPS updates are underway.** This release includes refresh-handling improvements, with further DLPS update work in progress. See the [release notes](https://github.com/kerrdec97/Game-Catalogue/releases/tag/v0.0.3).

## Licence, privacy, and notices

Game Catalogue is proprietary software licensed for personal, non-commercial use. Redistribution, modification, and reverse engineering are prohibited except where applicable law permits.

- [Proprietary software licence](LICENSE.txt)
- [Privacy notice](PRIVACY.md)
- [Third-party notices](THIRD_PARTY_NOTICES.txt)
- [Release checksums](SHA256SUMS.txt)

---

## Credits

- **DeckerR97** — [GitHub](https://github.com/kerrdec97) · [Ko-fi](https://ko-fi.com/deckerr97)
- **Nazky** — [GitHub](https://github.com/Nazky) · [Ko-fi](https://ko-fi.com/nazkyyt)
- **Pippo26442999** — [GitHub](https://github.com/Pippo26442999) · [Ko-fi](https://ko-fi.com/pippo26442999)

Game library sourced from [dlpsgame.com](https://dlpsgame.com).
