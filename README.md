# Seminary Communicators — Vercel deploy

## Files
- `index.html` — the hub
- `content.json` — all editable content (guide, video link, days)
- `vercel.json` — disables caching so edits appear immediately

All three must sit at the **root of the repo**, not in a subfolder.

## Deploy
1. Push these files to the root of your GitHub repo (`Seminary-Communicators`).
2. vercel.com → **Add New… → Project** → import the repo.
3. Framework Preset: **Other**. Leave Build Command and Output Directory blank.
4. **Deploy**. You get a URL like `seminary-communicators.vercel.app`.

## Custom domain
Vercel → Project → **Settings → Domains** → add your domain, then add the DNS records Vercel shows at your registrar.

## Editing
1. GitHub → avatar → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Repository access: **Only select repositories** → your repo.
3. Permissions → **Contents: Read and write**. Generate and copy the token.
4. Open your site → footer → **Editor Access** → paste the token.

The token is stored in your browser only. Edits save to `content.json` in the repo; Vercel redeploys automatically and the live site updates in under a minute.

## Uploading files (PDFs, series graphics)
Put them in the repo root (or an `assets/` folder) and reference them by path. They deploy with the site and download natively.
