echo "# Lyric Display App – Updates Repository

This repository is used **exclusively** for hosting update files for the Lyric Display desktop app.

## Purpose
When new versions of the app are built and published, release assets (installers, update packages, and \`latest.yml\` metadata) are automatically uploaded here by the **Electron auto-update** system.

The main source code for the Lyric Display app is located in:
👉 [Lyric Display App Main Repository](https://github.com/PeterAlaks/lyric-display-app) which is a private repo.

## How It Works
- **electron-builder** publishes new releases here.
- The app checks this repository’s GitHub releases for updates.
- Users receive automatic update prompts in the app.

⚠️ This repo is **not** meant for manual code changes or contributions." > README.md
