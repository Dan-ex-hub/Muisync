# Upstream Attribution & Project Lineage

## Original Project

- **Project Name:** SynQ Browser Extension
- **Original Upstream Repository:** [https://github.com/SynQApp/Extension](https://github.com/SynQApp/Extension)
- **Original Upstream Baseline Commit:** `a8ed930` (*"Change Spotify to UI controlled rather than API controlled (#77)"*)
- **License:** Apache License, Version 2.0 (Apache-2.0)
- **Original Authors & Maintainers:** SynQ, LLC and upstream contributors (including Michael Lockwood, Rachael Meziere, Garret Janeczko, Donnie Li, and community contributors).

---

## Derivative Project: MuiSync

**MuiSync** is an independent, student-maintained derivative of the SynQ Browser Extension, developed for an open-source software contribution coursework project (ROSPL).

### License & Attribution Compliance

In compliance with the Apache License, Version 2.0 (in particular, Sections 4(a), 4(b), and 4(c)):

1. **License Retention:** The original `LICENSE` file containing the full Apache-2.0 license text is preserved intact in this repository.
2. **Attribution:** The original authors, contributors, and upstream repository are fully acknowledged. This project does not claim original authorship of the pre-existing codebase.
3. **Modification Notices:** Modifications made to files in this derivative retain existing notices and carry clear attribution of derivative changes.
4. **No Endorsement:** MuiSync is an independent student academic project and is not affiliated with, endorsed by, or an official release of SynQ, LLC or the original SynQ maintainers.

---

## Architectural & Functional Lineage

### Inherited from Upstream SynQ
- Core adapter architecture interfacing with supported music services.
- Mini player popup and floating Picture-in-Picture (PiP) player.
- Cross-platform link conversion and redirect popup flow.
- Redux Toolkit store architecture, actions, and persistent settings.
- Plasmo browser extension framework build system (Chrome & Edge MV3).
- Underlying service integration for Spotify, Apple Music, YouTube Music, and Amazon Music.

### Changes Made in this Derivative
- **Brand Identity & Assets:** Rebranded visible product surfaces to MuiSync (`mui-sync`), featuring an original music-themed logo (an 'M' combined with dynamic soundwave and equalizer geometry) and updated extension icons.
- **Coursework Maintenance & Bug Fixes:**
  - YouTube Music like/dislike status resolution (`fix/ytm-like-status`).
  - Redux-persist rehydration race condition prevention on startup (`fix/settings-rehydration-race`).
  - Routing of tab query and manipulation calls to the background service worker to prevent content script refresh loops (`fix/tabs-in-background-worker`).
  - Spotify artist metadata de-duplication and queue population in Picture-in-Picture mode (`fix/spotify-metadata-and-queue`).
