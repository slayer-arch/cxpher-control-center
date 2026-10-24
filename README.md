# Cxpher Control Center

A hand-coded, responsive sci-fi command dashboard for an Android tablet, hosted with GitHub Pages.

## Current status: v0.1.0 frontend prototype

Includes:
- Responsive dashboard layout for tablet, desktop, and mobile
- Live local clock and date
- Overview, Environment, Systems, Security, and Settings navigation
- Simulated room-control toggles
- Session activity stream
- Sample sensor reading preview
- Theme accent toggle and clear-log action
- Explicit demo-mode labels so simulated controls are not mistaken for real hardware control

Not yet included:
- ESP32 telemetry
- Physical light/device control
- PC hardware monitoring
- Home Assistant integration
- Authentication or backend APIs

## Repository structure

```text
cxpher-control-center/
├── index.html
└── README.md
```

## Publish with GitHub Pages

1. Create a GitHub repository named `cxpher-control-center`.
2. Set visibility to **Public** if using GitHub Free and standard GitHub Pages.
3. Upload `index.html` and `README.md` to the repository root.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, select **Deploy from a branch**.
6. Select branch `main` and folder `/ (root)`, then save.
7. Wait for deployment and open the published URL shown on the Pages settings screen.

The URL usually looks like `https://YOUR-USERNAME.github.io/cxpher-control-center/`. Use the exact URL GitHub displays.

## Test locally first

Open `index.html` in a modern browser. The interface does not need a build step or external libraries.

## Open on the Cidea tablet

1. Open the published GitHub Pages URL in the tablet browser.
2. Rotate the tablet to landscape.
3. In the browser menu, choose **Add to Home screen** if available.
4. Once stable, we can configure a kiosk app or pin the browser using Android's supported screen-pinning feature.

## Architecture notes

GitHub Pages serves static files. JavaScript in this page cannot safely or reliably discover arbitrary devices on your local Wi-Fi, read Windows hardware sensors, or directly control physical devices. Those features require a backend or a supported integration, for example a Home Assistant server, a local PC agent, or an ESP32 endpoint designed with appropriate access controls.

Do not put passwords, API keys, Home Assistant long-lived tokens, or other secrets in this repository or browser-side JavaScript. Public GitHub repositories are public, and client-side secrets are visible to visitors.

## Suggested next milestones

- v0.2: refine tablet landscape layout and add persistent preferences
- v0.3: connect ESP32 sensor data through a secured local integration
- v0.4: integrate Home Assistant for compatible devices
- v0.5: add Windows PC telemetry via a local agent
