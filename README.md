# ganlin-site

甘霖 (Gan Lin) 的个人落地页 — a single-file WebGL personal landing page.

Inspired by [haoqi.design](https://haoqi.design): a deep, cool iridescent **light field** plus a **refractive glass orb** with chromatic dispersion, all in one hand-written GLSL fragment shader (raw WebGL, **no CDN dependency** — works behind the GFW). Editorial glassmorphism content layered on top (Fraunces + Inter).

## Stack
- Pure single-file `index.html` (inline CSS/JS, raw WebGL shader)
- No framework, no build step, no `package.json`
- Fonts: Google Fonts (Fraunces / Inter / Space Grotesk) with system fallbacks

## Run locally
```bash
python3 -m http.server 8731 --directory .
# open http://localhost:8731
```

## Deploy (Zeabur, 国内可访问)
- `Dockerfile` (nginx:alpine, port 8080) is included.
- Push to GitHub → import on Zeabur → it auto-detects the Dockerfile.
- Do **not** add a `package.json` (Zeabur would misdetect it as a Node app → 502).

## Edit content
All copy lives directly in `index.html` sections: `#about`, `#work`, `#capabilities`, `#contact`.
