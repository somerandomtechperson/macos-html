# macOS Web — Browser Desktop Simulator

A browser-based desktop simulator inspired by the look and feel of macOS. It recreates desktop UI elements such as a translucent menu bar, Dock, desktop icons, window controls, and familiar built-in-app-style interfaces using web technologies.

> **This is a fan-made browser simulation, not macOS.** It does not run native Mac applications and is not affiliated with or endorsed by Apple Inc.

## Features

- **macOS-inspired desktop UI** with a menu bar, Dock, desktop icons, and translucent surfaces.
- **Startup sequence** with an Apple-inspired boot screen and startup audio.
- **Window management** including moving, resizing, minimizing, maximizing, and switching between app windows.
- **Built-in-style apps** including Finder-inspired file browsing, Calculator, Calendar, Notes, Safari-style browsing, Photos, System Settings, and a code-editor-style interface.
- **Appearance controls** including bundled wallpaper choices and desktop customization.
- **Self-contained edition** with artwork, icons, and audio embedded into a single HTML file.
- **Browser-based** — no native installer is required for the standalone edition.

Some apps are visual simulations; functionality is not identical to the corresponding macOS apps.

## Run it in a browser

### Standalone HTML edition

1. Download or clone this repository.
2. Open `macos-web-standalone.html` in a recent version of Chrome, Edge, Firefox, or Safari.
3. Wait for the startup sequence to finish, then use the desktop and Dock to open apps.

The standalone HTML edition does not require Node.js, npm, or a local web server. Some features that visit external websites still require an internet connection.

### Run the Svelte source version

The source project uses **Svelte**, **Vite**, and **TypeScript**. To run the development version, install a recent compatible version of Node.js, then enable Corepack and install the dependencies:

```bash
corepack enable
pnpm install
pnpm dev
```

Open the local URL printed by Vite in your browser.

Useful commands:

```bash
pnpm check   # Run Svelte and TypeScript checks
pnpm build   # Build the production site into dist/
pnpm serve   # Preview the production build locally
```

The source version needs its package dependencies installed. The standalone HTML edition is intended for quick use without a build step.

## Project layout

```text
.
├── macos-web-standalone.html  # Optional single-file browser edition
├── index.html                 # Vite/Svelte app entry point
├── src/                       # Svelte components, app interfaces, and styles
├── public/                    # Static assets such as icons and audio
├── package.json               # Dependencies and development scripts
├── pnpm-lock.yaml             # Locked dependency versions
└── LICENSE                    # Project license
```

The standalone HTML file is a separate, self-contained browser edition. It is not a direct build output of the Svelte source tree, so some details and app behaviors may differ between the two versions.

## Compatibility

Use a modern desktop browser for the best experience. The layout is designed primarily for mouse and keyboard input; small screens may have a more limited experience. Browsers may restrict certain behaviors when an HTML file is opened directly from disk.

## Contributing

Suggestions, bug reports, and improvements are welcome. When reporting a problem, please include the browser you used, what you expected to happen, and steps to reproduce it. For code changes, open a pull request with a concise description of the changes.

## Credits and license

The included Svelte source project identifies itself as an open-source macOS desktop recreation and includes an MIT license. Keep the included `LICENSE` file with the source when redistributing it, and review any applicable terms for third-party assets before publishing modified or bundled versions.

macOS and Apple are trademarks of Apple Inc. All product names and visual references are used descriptively; this project is not an official Apple product.
