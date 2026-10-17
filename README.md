# eashaan.runs-on.dev

Single-file portfolio. No build step, no framework, no dependencies besides Google Fonts.

## Files
- `index.html` - the whole site (HTML, CSS, JS inline)
- `img/` - research thumbnails (from your old site, compressed to WebP)
- `CNAME` - tells GitHub Pages to serve this repo at `eashaan.runs-on.dev`
- `resume.pdf` - **add this yourself** (export your current Word resume to PDF). The "Resume (PDF)" button and command-menu entry link to it.

## Deploy on GitHub Pages
1. Put `index.html`, `CNAME`, the `img/` folder and `resume.pdf` at the root of your `eashaanmano.github.io` repo (replacing the old files; keep the old ones in a branch if you want a backup).
2. Repo Settings > Pages: source = deploy from branch `main`, folder `/ (root)`. Custom domain = `eashaan.runs-on.dev`. Tick "Enforce HTTPS" once the certificate is issued.
3. In your runs-on.dev dashboard, point the subdomain with a **CNAME record** to `eashaanmano.github.io`.
4. Wait for DNS (minutes to a few hours). `eashaanmano.github.io` will then redirect to the new domain automatically.

## Editing
- Text lives directly in `index.html`; search for the section id (`id="work"`, `id="projects"`, ...).
- Project status chips: remove `<span class="chip wip">In active development</span>` from LedgerFlow / OrderBook once their repos are public, and change their "Follow on GitHub" links to the repo URLs.
- Lens tags: any element with `data-t="sys"`, `data-t="ml"` or `data-t="ml sys"` reacts to the SDE / ML switch.
- Research filter counts update automatically from the `data-k` attribute on each `<li class="pub">`.

- Toolkit: each tool in the terminal is marked ● (used in shipped work) or ○ (working knowledge). Search `const TOOLKIT` in `index.html`; change a tool's `'f'` to `'s'` once you've used it in a project, or add a row `['Name', null, 's', 'sys']`.
- Terminal commands: `help`, `ls`, `ls <area>`, `grep <word>`, `shipped`, `view sde|ai|all`, `whoami`, `contact`, `raft crash`, `clear` (and one hidden one: try `sudo hire eashaan`).

## Share-ready links
- `https://eashaan.runs-on.dev/#swe` opens the site pre-set to the SDE view
- `https://eashaan.runs-on.dev/#ai` opens it pre-set to the AI, ML and data view
