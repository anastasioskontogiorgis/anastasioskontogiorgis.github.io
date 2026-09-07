# Portfolio site — deploy & fill-in guide

A hand-built static site: no build step, no framework — edit the HTML, push, done.

## Files

- `index.html` — landing page (hero, four project case files — three live, one in progress — research teaser, contact)
- `research.html` — the research page (NoisyGraph story, figures, publications)
- `styles.css` — all styling (design tokens at the top)
- `assets/` — the three thesis figures (+ your portrait, later)

## 1 · Fill the placeholders (before publishing!)

Every placeholder is a `[[TOKEN]]` you can find-and-replace. List them all with:

```bash
grep -n "\[\[" index.html research.html
```

| Token | What goes there |
|---|---|
| `[[EMAIL]]` | Your permanent personal email (appears 4×: hero, both footers) |
| `[[LINKEDIN_URL]]` | LinkedIn profile URL |
| `[[SCHOLAR_URL]]` | Google Scholar profile URL (index + research page) |
| `[[BOOK_DEMO_URL]]` | Hugging Face Space URL of the book recommender |
| `[[BOOK_REPO_URL]]` | GitHub repo URL of the book recommender |
| `[[PHISHING_SERVICE_URL]]` | The deployed phishing service URL (when live) |
| `[[CAMPAIGN_REPO_URL]]` | GitHub repo URL of the campaign-uplift project (or delete the anchor until the repo exists) |
| `[[CV_PDF_URL]]` | Link to a PDF export of your CV — or delete that link if you prefer CV-on-request |

If a link isn't ready yet (e.g. the phishing service), either fill it with the
GitHub repo URL temporarily or delete the anchor — don't publish a `[[TOKEN]]`.

## 2 · Add your photo (when ready)

In the header of **both** pages, replace

```html
<span class="avatar">AK</span>
```

with

```html
<span class="avatar"><img src="assets/portrait.jpg" alt="Anastasios Kontogiorgis"></span>
```

and drop `portrait.jpg` (square crop works best) into `assets/`. Until then, the
navy AK monogram is the intentional placeholder — it looks finished, not missing.

## 3 · Publish (GitHub Pages, root domain)

```bash
# one-time: create a repo named EXACTLY  anastasioskontogiorgis.github.io
git init && git add . && git commit -m "portfolio site"
git branch -M main
git remote add origin https://github.com/anastasioskontogiorgis/anastasioskontogiorgis.github.io.git
git push -u origin main
```

GitHub Pages serves user-site repos automatically from `main` — the site appears
at **https://anastasioskontogiorgis.github.io/** within a couple of minutes
(Settings → Pages to confirm). Your Ethereum project keeps living happily at
`/ethereum-fraud-analysis/` alongside it.

## Design notes (so future edits stay coherent)

- Tokens live at the top of `styles.css`; the palette is your CV's navy plus a
  cool paper base and one warm accent.
- The signature element is the signal-from-noise motif: the hero line decodes
  from channel noise on load (skipped for reduced-motion visitors), and the
  divider line resolves from dashed "noise" into solid "signal". One accessory
  — everything else stays quiet on purpose.
- The project rows lead with a number in mono. If you add a project, keep that
  pattern: status eyebrow, one measured metric, prose, tags, links. For a
  not-yet-live project, use `class="status wip"` on the eyebrow so it renders
  grey instead of the active accent (the campaign-uplift card does this).
