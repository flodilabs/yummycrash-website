# YummyCrash Legal Pages

Static website hosting the Privacy Policy and Terms of Service for the
YummyCrash mobile game.

## Hosting via GitHub Pages

1. Create a new GitHub repository named **`yummycrash-legal`** under your
   account (`burakerol`):
   - Go to https://github.com/new
   - Repository name: `yummycrash-legal`
   - Public visibility (required for GitHub Pages free tier)
   - Don't initialize with anything — leave it empty

2. Upload these files to the repository root:
   - `index.html`
   - `privacy.html`
   - `terms.html`
   - `style.css`

   Easiest method via the web UI:
   - On the new repo page, click "uploading an existing file"
   - Drag all four files in, commit directly to `main`

3. Enable GitHub Pages:
   - Repo → Settings → Pages (left sidebar)
   - Source: **Deploy from a branch**
   - Branch: **`main`** · folder: **`/ (root)`** · Save
   - Wait ~1 minute, then refresh — GitHub shows the live URL

4. Your live URLs will be:
   - Home:    `https://burakerol.github.io/yummycrash-legal/`
   - Privacy: `https://burakerol.github.io/yummycrash-legal/privacy.html`
   - Terms:   `https://burakerol.github.io/yummycrash-legal/terms.html`

These URLs already match what's set in `src/config/storeConfig.ts`. No app
changes needed.

## Verifying before submission

After enabling Pages, open the URLs in an **incognito window** (not signed in
to GitHub) to confirm they're publicly accessible. Apple's reviewers will hit
them from outside any login. If they 404 or hit a login wall, the submission
will be rejected.

## Moving to Vercel later

If you want to switch hosting to Vercel down the line:

1. Sign in to https://vercel.com
2. Import the GitHub repo
3. Deploy (no build step needed — it's pure static HTML)
4. Optional: connect a custom domain
5. Update the two URLs in `src/config/storeConfig.ts` and rebuild the app

Static HTML is portable — these files work on any static host (Vercel,
Netlify, Cloudflare Pages, your own server, etc.).

## Updating the legal text

If you ever update the in-app Privacy Policy or Terms text (in
`src/components/SettingsPopup.tsx`), also update the matching `.html` files
here and re-deploy. The in-app text and the public URL should stay in sync.
