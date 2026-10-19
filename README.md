# Lekha launchers

Home-screen launchers for Lekha client apps (AiSME OS). Softr's Basic plan sends phones no home-screen icon, so each client gets a small page here that carries the Lekha icon and opens the client's Softr app.

Live: `https://aismecambodia.github.io/lekha/<client>/`

| Client | Launcher | Opens |
|---|---|---|
| U2BE | /lekha/u2be/ | https://lekha-u2be.softr.app/ |
| AiSME (master) | /lekha/aisme/ | https://aisme-os.softr.app/ |

## How it works

- The user opens the launcher once and taps Add to Home Screen.
- **Android:** on first load the page rewrites its own address to `?go=1`; the saved shortcut carries it and redirects straight to the Softr app.
- **iPhone:** iOS re-loads the saved address to fetch the icon, so the page stays plain (no `?go=1`, no redirect) and iOS finds the Lekha icon. The icon opens in standalone mode (`apple-mobile-web-app-capable`), which redirects to the Softr app. (19 Oct fix: the old `?go=1` logic made iOS fetch Softr's page and show a grey letter icon.)

## Add a client

1. Copy `u2be/` to `<client>/`.
2. In `<client>/index.html`, change `TARGET` and the names.
3. In `<client>/manifest.webmanifest`, change `name` and `short_name`.
4. Commit to `main`. GitHub Pages publishes in about a minute.

Icons: Lekha icon on full-bleed indigo `#3D2B8E` (no transparent corners, which iOS fills black).
