# Counter — installable app

This folder is a complete installable web app (PWA). Once it's hosted
somewhere, you can add it to your phone's home screen and it opens like a
normal app — full screen, its own icon, and it keeps working without
internet after the first load.

## Why it needs to be hosted (quick version)

Phones only allow "install to home screen" for sites served over **https://**.
Opening `index.html` straight from a Downloads folder won't offer the install
prompt. You need to put these files on a free static host first. Takes about
2 minutes.

## Easiest option: Netlify Drop (no account needed to try it)

1. Go to **app.netlify.com/drop** in a browser.
2. Drag this whole folder onto the page.
3. It gives you a live `https://something.netlify.app` link.
4. Open that link on your phone.

## Equally easy: GitHub Pages / Vercel / Cloudflare Pages

Any static host works — just upload all the files in this folder, keeping
the same structure (`index.html`, `manifest.json`, `service-worker.js`,
`icons/` folder together, all at the same level).

## Installing on your phone

**Android (Chrome):** open the link → tap the **⋮** menu → **"Add to Home
screen" / "Install app"**.

**iPhone (Safari):** open the link → tap the **Share** icon → **"Add to Home
Screen"**. (Must be Safari — Chrome on iOS can't install PWAs.)

After that, it shows up as a normal app icon. It opens full-screen and keeps
your products and sales saved on that device even with no signal.

## Files in this folder

- `index.html` — the whole app
- `manifest.json` — tells the phone it's installable, sets the icon/name
- `service-worker.js` — caches the app so it works offline after first load
- `icons/` — home screen icons
