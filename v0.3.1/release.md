# Local RAG Companion v0.3.1

Released 2026-08-31.

- Fixed the companion crashing on every launch with `ReferenceError: DOMMatrix is not defined`. `server/services/extractors.ts` imported `pdf-parse` at module load time, which pulls in `pdfjs-dist`'s Node canvas polyfill setup unconditionally - the compiled binary has no DOM and no bundleable native canvas addon, so the daemon died before the dashboard was even reachable, regardless of whether a PDF was ever opened. The import is now deferred until a PDF is actually indexed.
- Fixed the v0.3.0 macOS installer failing to launch at all on a fresh Mac (`spctl`: "invalid signature (code or signature have been modified)", SIGKILL on launch, not a normal Gatekeeper prompt - no "Open Anyway" override could fix it). The packaged `.app` is now re-signed (ad-hoc) as the last packaging step, after every file is in place.
- macOS-only release - Windows/Linux installers are unchanged from 0.3.0 pending a rebuild on those platforms.

## Included

| Platform | File | Size | SHA-256 |
| --- | --- | --- | --- |
| macOS (Apple Silicon) | `Local-RAG-Companion-macOS-arm64.dmg` | 56.8 MB | `88d2bbac1bd0897818ec5d41973271fadc0036bb523e91202cc68e52abfdb73c` |
