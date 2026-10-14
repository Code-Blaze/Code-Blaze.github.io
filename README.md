# Code Blazer — Portfolio of Saptarshi Mazumder

**Live site:** https://code-blaze.github.io

An interactive, threat-intelligence-themed portfolio. Visitors play an analyst tracking an
elusive white-hat actor known only as **Code Blazer**, pull the attribution report from a sealed
archive, and declassify it to reveal who is behind the alias.

## How it plays

1. **The hunt.** A Kali-style terminal builds a threat actor profile, correlates personas and
   decrypts the dossier.
2. **The reveal.** The screen glitches and flickers into 3D Matrix rain, and the decrypted
   attribution report opens with a single action: **[ DECLASSIFY ]**.
3. **The portfolio.** An interactive `analyst@matrix` terminal (`help`, `about`, `achievements`,
   `projects`, `education`, `career`, `skills`, `contact`), plus a **Simple view** for readers
   who prefer a regular page.

Returning visitors skip straight to the portfolio; **Replay intro** (or the `replay` command)
plays the story again. The intro is entirely fictional, cinematic flavour text.

## Under the hood

- Plain HTML, CSS and JavaScript in a single `index.html`, with no build step or framework.
- All portfolio content lives in one `DATA` object, which feeds both the terminal and the simple view.
- Live TryHackMe rank via TryHackMe's official badge, framed and recoloured to fit the theme.
- Respects `prefers-reduced-motion`, works at phone width, and falls back to a built-in 2D rain
  if the 3D engine's files can't be loaded.

## Run locally

The 3D rain loads its assets with `fetch`, so serve the folder over HTTP rather than opening
the file directly:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Credits

- 3D digital rain: [Rezmason/matrix](https://github.com/Rezmason/matrix), MIT License
  (see `matrix/LICENSE`).
- Fonts: Share Tech Mono and IBM Plex Sans via Google Fonts.
