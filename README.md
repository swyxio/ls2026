# DEPRECATED

This prototype has moved to a different repo. Do not build on this one.

---

# ls2026 — Latent Space landing page prototype

Static mockup of the 2026 Latent Space landing page (Richard's wireframe), built performance-first.

## Run

```sh
npx serve .        # or: python3 -m http.server
```

Open `index.html` directly in a browser also works — there is no build step.

## Performance choices

- One HTML file, one request. CSS is inlined; no JavaScript, no web fonts, no images.
- Dropdown nav menus and the expandable AI News stories (Techmeme-style) use native `<details>/<summary>`, so they work without JS and are keyboard accessible.
- System font stack, CSS grid layout, `aspect-ratio` placeholders so nothing shifts when real images/cover art arrive (zero CLS).
- Sticky AI News rail on desktop, single column under 980px.

## Layout (from wireframe)

```
Masthead: wordmark · tagline · search · Subscribe
Nav: Articles · AI News · Podcasts ▾ · Watch · More ▾      About · Contribute · Archive · Social
┌──────────────────────────────┬──────────────┐
│ Top story                    │ AI News      │
│ 2nd story   │ 3rd story      │ top stories  │
├──────────────────────────────┼──────────────┤
│ Main podcast recent episodes │ Other shows  │
├──────────────────────────────┴──────────────┤
│ Popular posts (3)                           │
├─────────────────────────────────────────────┤
│ Footer: subscribe · explore · about · follow│
└─────────────────────────────────────────────┘
```

All headlines and links are placeholders.
