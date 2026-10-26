# MuiSync Browser Extension

<p align="center">
  <img src="assets/icon-128.png" width="96" height="96" alt="MuiSync Logo" />
</p>

<p align="center">
  <strong>Your universal music companion for controlling playback and opening music links across Spotify, Apple Music, YouTube Music, and Amazon Music.</strong>
</p>

<p align="center">
  An open-source browser extension for Google Chrome and Microsoft Edge (Manifest V3).
</p>

---

> [!NOTE]
> **Project Origin & Attribution:**
> **MuiSync** is an independent, student-maintained derivative of the original [SynQ Browser Extension](https://github.com/SynQApp/Extension) (baseline commit [`a8ed930`](https://github.com/SynQApp/Extension/commit/a8ed930)), developed as part of an open-source software contribution coursework project (ROSPL). This project is licensed under the **Apache License, Version 2.0**. Full upstream attribution, copyright notices, and lineage details are documented in [UPSTREAM.md](UPSTREAM.md).

---

## Features

- 🎵 **Multi-Platform Integration:** Seamlessly controls playback across the web players of major music streaming services.
- 🔗 **Cross-Platform Link Redirects:** Receive a song link on a platform you don't use? MuiSync intercepts it and offers to open the matching track, album, or artist on your preferred service.
- ⚙️ **Comprehensive Playback Controls:** Play, pause, skip, seek, adjust volume, toggle repeat, and manage like/dislike states directly from a compact mini player.
- 🔄 **Queue Inspection:** Browse upcoming tracks and jump straight to songs in your queue without leaving your current tab.
- 🔊 **Floating Picture-in-Picture Mode:** Detach the player into a floating, always-on-top window for effortless control across all browser tabs and applications.
- 🎉 **Track Notifications:** Instant background notifications keep you informed whenever the current track changes.
- ⌨️ **Keyboard Controls:** Integrated keyboard shortcuts for rapid, friction-free music management.

---

## Supported Music Services

MuiSync supports the following web music services:

- **Spotify** (`open.spotify.com`)
- **Apple Music** (`music.apple.com`)
- **YouTube Music** (`music.youtube.com`)
- **Amazon Music** (`music.amazon.com`)

---

## Technology Stack

- **Core & Runtime:** TypeScript, Chrome Manifest V3 (MV3)
- **Framework & Extension Tooling:** [Plasmo Framework](https://www.plasmo.com/)
- **UI:** React 18, `styled-components`, `@synqapp/ui` component library
- **State Management:** Redux Toolkit with `redux-persist`
- **Package Manager:** `pnpm`

---

## Development & Setup

### Prerequisites

- [Node.js](https://nodejs.org/) (v18+ recommended)
- [pnpm](https://pnpm.io/) package manager:
  ```bash
  npm install -g pnpm
  ```

### Installation

Clone the repository and install dependencies:

```bash
pnpm install
```

### Building the Extension

To build production bundles for Chrome or Edge:

```bash
# Chrome (Manifest V3)
pnpm build

# Microsoft Edge (Manifest V3)
pnpm build --target=edge-mv3
```

The compiled extension will be output to:
- `build/chrome-mv3-prod/` (Chrome)
- `build/edge-mv3-prod/` (Edge)

### Loading the Extension in Your Browser

1. Navigate to `chrome://extensions/` (Chrome) or `edge://extensions/` (Edge).
2. Enable **Developer mode** (toggle in the top-right corner on Chrome, or left sidebar on Edge).
3. Click **Load unpacked**.
4. Select the `build/chrome-mv3-prod/` (or `build/edge-mv3-prod/`) directory.
5. The MuiSync icon will appear in your extensions toolbar.

### Development Mode

To run a live development server with hot module reloading:

```bash
pnpm dev
```

### Useful Scripts

| Command | Description |
| ------- | ----------- |
| `pnpm build` | Compiles a production Chrome MV3 build into `build/chrome-mv3-prod/` |
| `pnpm build --target=edge-mv3` | Compiles a production Edge MV3 build into `build/edge-mv3-prod/` |
| `pnpm dev` | Starts development mode with watch and hot reloading |
| `pnpm format:all` | Formats all source files with Prettier |
| `pnpm format:check` | Checks code formatting with Prettier |
| `npx tsc --noEmit` | Runs TypeScript type checking without emitting files |

---

## License & Attribution

This project is licensed under the **Apache License, Version 2.0** (`Apache-2.0`). See the [LICENSE](LICENSE) file for complete license terms.

### Upstream Credits

MuiSync builds upon the foundational architecture and contributions of the original **SynQ** project. We extend our sincere gratitude to the original creators and contributors:

- **Michael Lockwood** ([@mlockwood](https://github.com/mlockwood))
- **Rachael Meziere**
- **Garret Janeczko**
- **Donnie Li** ([@dongyangli1226](https://github.com/dongyangli1226))
- Upstream contributors to [SynQApp/Extension](https://github.com/SynQApp/Extension)

For detailed information on the relationship between MuiSync and the upstream SynQ project, please refer to [UPSTREAM.md](UPSTREAM.md).
