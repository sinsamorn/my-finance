# My Financial Dashboard

A Progressive Web App (PWA) for tracking income, expenses and monthly bank payments.

- **Hosting:** GitHub Pages (static files, no build step)
- **Login and sync:** Supabase (email + password, one row of data per user, protected by row-level security)
- **Offline:** works without internet; changes upload when you're back online

## Files
| File | What it is |
|---|---|
| `index.html` | The whole app (layout, styles and code) |
| `supabase.js` | Supabase client library (v2.119.0), bundled so it works offline |
| `sw.js` | Service worker for offline use |
| `manifest.json`, `icon-*.png` | App name and icons for "Install" / "Add to Home Screen" |

## Turn on GitHub Pages
Settings → Pages → Source: **Deploy from a branch** → Branch: **main**, folder **/ (root)** → Save.
The app appears at `https://<your-username>.github.io/my-finance/`.

## Supabase settings to check once
Authentication → URL Configuration:
- **Site URL:** `https://<your-username>.github.io/my-finance/`
- **Redirect URLs:** add the same address

This makes the confirmation and password-reset emails open the app.
