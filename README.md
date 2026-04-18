# promptomate-landing

Static marketing site for [Promptomate](https://github.com/guttaashok1/promptomate). Zero build step, single HTML file, ~20 KB.

## Deploy

### Vercel (recommended)

```bash
# First time — install Vercel CLI if you don't have it
npm install -g vercel

# From this directory
vercel       # follow prompts, link to your Vercel account
# next time:
vercel --prod
```

Vercel auto-detects a static site, no config needed. Takes ~30 seconds. You'll get a URL like `promptomate-landing.vercel.app` and can point a custom domain at it.

### Cloudflare Pages

1. Push this repo to GitHub
2. Go to https://pages.cloudflare.com → Create project → Connect to GitHub → pick this repo
3. Build command: _(leave empty)_
4. Build output directory: `/`
5. Deploy

### Netlify

```bash
npm install -g netlify-cli
netlify deploy --prod --dir=.
```

### GitHub Pages

1. Push to `main`
2. Repo Settings → Pages → Source: Deploy from branch `main`, `/ (root)`
3. Done

## Edit

Everything lives in `index.html`. CSS is inline. No framework, no bundler. Open in any browser to preview:

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## What to update before launch

- Replace the "Demo GIF — coming soon" placeholder with the real GIF (see [issue #5](https://github.com/guttaashok1/promptomate/issues/5))
- Add a favicon (optional)
- Custom domain (e.g. `promptomate.dev`) pointed at the deploy
- Open Graph image for social previews (optional — default is OK)

## License

MIT. Free to fork, steal, remix.
