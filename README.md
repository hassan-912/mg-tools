# MG Workspace

A separate, lightweight home page for three existing MG tools:

- Visa Calculator: tourism and immigration, hosted on Vercel.
- Notes: the existing Mawid application, hosted on Cloudflare Workers. Its name on this launcher is Notes; the existing application and its data are unchanged.
- Visa Review: the existing review application, hosted on Streamlit.

Each card is a normal HTTPS link that opens in a new tab. The launcher has no runtime dependencies, backend, embedded applications, analytics, shared authentication, or client-data storage. The linked applications keep their existing sign-ins and hosting. The launcher does not guarantee availability of a separately hosted tool or prevent that tool's host from sleeping.

## Local preview

From this directory, serve `dist` with a static HTTP server, for example:

```powershell
python -m http.server 4173 --bind 127.0.0.1 --directory dist
```

Open `http://127.0.0.1:4173`. No dependency installation or build is needed.

## Change a destination

Edit the card's `href` in `dist/index.html`. The company link in the header is separate from the three tool links.

## Publication

This directory is an independent Sites project. Its identity is stored in `.openai/hosting.json` and its static output is `dist/`. Preserve the assigned project ID when publishing updates.
