# Game Catalogue v0.0.3

Maintenance update with exFAT cover fixes and DLPS refresh-handling improvements, following [issue #1](https://github.com/kerrdec97/Game-Catalogue/issues/1).

## Fixes

- exFAT cover art now uses the image service already used by other tabs, with compatible JPEG output and a direct-image fallback. This applies to existing saved libraries without requiring another scrape.
- Direct cover URLs in the other tabs can also fall back to the image service if loading fails. Retries are bounded so failed images cannot loop indefinitely.
- Removed the mandatory full crawl of DownloadGamePS3 before a DLPS refresh. Only referenced archive posts are fetched, and an unavailable archive retains the original links instead of aborting the catalogue update.
- DLPS requests have timeouts and lower page concurrency. Invalid, empty, or failed pages stop the update before a partial catalogue can replace saved data.
- Improved DLPS update messages so users receive a readable explanation instead of only an exit code or stack-trace line.

## DLPS updates

DLPS updates are underway. This release includes refresh-handling improvements, with further DLPS update work in progress. The exFAT cover fix was verified in the packaged Windows application.

## Verification before publication

- 22 Python tests and 16 JavaScript tests passed.
- The six DLPS scraper regression tests also passed against the scraper and Node.js runtime extracted from the built EXE, including auxiliary-service handling, pagination safeguards, original-link preservation, and response validation.
- Live exFAT refresh and normalization passed with 759 records and 759 cover URLs.
- All 48 covers on the first alphabetical exFAT page downloaded and decoded as JPEG images.
- Launched the packaged v0.0.3 EXE and visually checked exFAT covers in the grid and details window. Existing DLPS and exFAT dataset files remained byte-for-byte unchanged during UI testing.

## Download and upgrade

Download the Windows x64 ZIP (recommended) or the standalone EXE. Close the previous version before running v0.0.3. Saved libraries and settings use the same application-data folder.

The ZIP contains the executable, proprietary licence, privacy notice, and third-party notices. No separate Node.js, npm, or Python installation is required. The application remains closed source; only release binaries and documentation are published.

See `SHA256SUMS.txt` for file verification.
