# Wreckd

A live cross-section of the Pons launchpad on Robinhood Chain (chain 4663).
Every launch sets sail, sails grow with volume, ten minutes of silence sinks a ship,
and the sharks are the wallets that buy within three seconds of a launch.

- `index.html` is the whole site: one page, no build step, no dependencies.
- It reads the public Robinhood Chain RPC directly from the browser. Read-only: no wallet, no keys.
- If the RPC cannot be reached (or the page is opened from disk), it plays a built-in recording of one real hour of Pons.
- `snapshot.json` is the same recording as a separate file; the page also carries a copy inline.

## Deploy

Netlify: Add new site → Import an existing project → GitHub → this repo. Leave the build command empty and the publish directory as `.` (already set in `netlify.toml`).

## Configure

At the top of the script in `index.html`, fill `CONFIG.TOKEN_CA` with the $WRECK contract after launch
(lights the lighthouse and enables Copy CA / Buy on Pons), `CONFIG.X_URL`, and `CONFIG.SITE_URL`.
