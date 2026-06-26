# Michelle On The Glow

The homepage for **Michelle Filsaime — Independent Beauty Consultant** ("Michelle On The Glow").

A single, self-contained landing page that wraps her Google Form sign-up
("Claim Your Complimentary Facial or Makeover") in a soft-luxe, on-brand design —
warm blush and champagne-gold tones, a glowing animated frame around the form,
and a neon-script nod to her event banner.

## What's here

- **`index.html`** — the whole page. No build step, no dependencies. Fonts load
  from Google Fonts; the form is embedded directly from Google Forms.
- **`favicon.svg` / `favicon.ico` / `favicon-32.png` / `favicon-16.png`** — the
  glow "M" monogram favicon (scalable SVG with `.ico`/PNG fallbacks).
- **`apple-touch-icon.png`** — 180×180 icon used when someone adds the site to
  their phone's home screen.

## Run it locally

Just open the file:

```bash
open index.html
```

Or serve it (optional):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publish it free with GitHub Pages

1. Push this repo to GitHub (done).
2. On GitHub: **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Branch: **`main`**, folder: **`/ (root)`**. Save.
5. After a minute the site is live at
   `https://mikefilsaime-groove.github.io/MichelleOnTheGlow/`.

To use a custom domain later (e.g. `michelleontheglow.com`), add it under
**Settings → Pages → Custom domain** and point the domain's DNS at GitHub Pages.

## Updating the form

The sign-up form is a Google Form embedded via `<iframe>` in `index.html`.
To swap it, replace the `src` URL inside the `.form-frame` iframe with the new
form's embed link (**Send → `< >` Embed HTML** in Google Forms).

> Note: Google Forms iframes use a fixed pixel height (`2382px` here, the value
> Google generated). If you change the form's questions, grab the new height from
> Google's embed code and update the `height` in `index.html` so nothing is clipped.
