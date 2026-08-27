# Local RAG Companion v0.3.0

Released 2026-08-27.

- Installers no longer bundle the Ollama runtime. They're roughly 4x smaller (macOS: 217MB -> 57MB; Windows and Linux drop by far more, since those also used to carry bundled CUDA/ROCm libraries).
- Added a "Set up local AI" button to the runner dashboard's LLM providers pane, which downloads and starts Ollama on demand instead - only if you actually want local models, not on every install.
- First release published to [local-runner-execute](https://github.com/YourAIAPPS-online/local-runner-execute) with full version history, alongside the existing R2-hosted downloads.

## Included

| Platform | File | Size | SHA-256 |
| --- | --- | --- | --- |
| macOS (Apple Silicon) | `Local-RAG-Companion-macOS-arm64.dmg` | 57.6 MB | `e47cfdd33d6d6c43570140e9bc1a256f13ec4b2ae286c85f6768dfc0db4435b6` |
| Windows (x64) | `Local-RAG-Companion-windows-x64.zip` | 69.8 MB | `94763feb63e8cfbdf329c0ab90bf44774a2b410e15062c55210f82bc97882ef8` |
| Linux (x64) | `Local-RAG-Companion-linux-x64.tar.gz` | 98.6 MB | `312bf3ea1a7ac433cdfd80cc86203f15c2a4a5f1cda7822deebb21593028e05c` |
