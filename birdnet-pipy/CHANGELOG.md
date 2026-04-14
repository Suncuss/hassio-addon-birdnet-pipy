
## 0.6.2-dev0 (2026-04-13)
- Simplify ingress nginx to a single `<base href>` rewrite. The frontend now declares `<base href="/">` in `index.html` and uses relative paths for all internal URLs (built assets via Vite `base: './'`, axios via `BASE + 'api'`, socket.io via `path: BASE + 'socket.io'`). Previous seven `sub_filter` rules (href/src/`/api`/`/socket.io`) are no longer needed and have been removed — the one `<base href>` replacement is now the sole source of the ingress path prefix.
- Fixes incidental brittleness caused by byte-level `sub_filter` matches in minified JS bundles (e.g. the old `/stream/` rule inadvertently double-prefixed `api.get("/stream/config")`).
- Update to latest version from Suncuss/BirdNET-PiPy (changelog: https://github.com/Suncuss/BirdNET-PiPy/releases)

## 0.5.5 (2026-03-02)
- Update to latest version from Suncuss/BirdNET-PiPy (changelog : https://github.com/Suncuss/BirdNET-PiPy/releases)
## 0.5.4-3 (26-02-2026)
- Minor bugs fixed
## 0.5.4-2 (23-02-2026)
- Fix Icecast service failing to connect to PulseAudio on HAOS by respecting PULSE_SERVER env var and setting up socket symlink and auth cookie for icecast2 user

## 0.5.4 (2026-02-21)
- Update to latest version from Suncuss/BirdNET-PiPy (changelog : https://github.com/Suncuss/BirdNET-PiPy/releases)
## 0.5.0-6 (15-02-2026)
- Minor bugs fixed
## 0.5.0-5 (15-02-2026)
- Minor bugs fixed
## 0.5.0-4 (2026-02-15)
- Disable nginx service when ingress is not active

## 0.5.0-3 (2026-02-15)
- Fix nginx startup without ingress by removing templated resolver dependency

## 0.5.0-2 (2026-02-14)
- Skip ingress nginx configuration when ingress is not active (empty/invalid ingress port)

## 0.5.0 (2026-02-14)
- Update to latest version from Suncuss/BirdNET-PiPy (changelog : https://github.com/Suncuss/BirdNET-PiPy/releases)

## 0.4.0 (2026-02-07)
- Update to latest version from Suncuss/BirdNET-PiPy (changelog : https://github.com/Suncuss/BirdNET-PiPy/releases)
## 0.3.2-6 (01-02-2026)
- Minor bugs fixed
## 0.3.2-5 (01-02-2026)
- Minor bugs fixed
## 0.3.2-4 (31-01-2026)
- Minor bugs fixed
## 0.3.2-2 (31-01-2026)
- Minor bugs fixed

## 0.3.2-3 (2026-01-30)
- Build frontend with /birdnet/ base path and serve under /birdnet/ for ingress compatibility.
## 0.3.2 (2026-01-30)
- Update to latest version from Suncuss/BirdNET-PiPy (changelog : https://github.com/Suncuss/BirdNET-PiPy/releases)
## 0.6.6 (30-01-2026)
- Minor bugs fixed
## 0.6.5 (30-01-2026)
- Minor bugs fixed
## 0.6.3 (29-01-2026)
- Minor bugs fixed
## 0.6.2 (29-01-2026)
- Use upstream nginx.conf and generate ingress config at startup
## 0.6.1 (29-01-2026)
- Minor bugs fixed
## 0.2 (29-01-2026)
- Minor bugs fixed
# Changelog

## 0.1.0

- Initial BirdNET-PiPy add-on with ingress support.
