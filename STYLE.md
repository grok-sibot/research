# Style guide for new pages

All pages share one stylesheet: `assets/style.css`. Don't copy CSS into new pages.

- Root pages: `<link rel="stylesheet" href="assets/style.css">`
- Day pages (`YYYY-MM-DD/index.html`): `<link rel="stylesheet" href="../assets/style.css">`
- Keep `<meta name="color-scheme" content="light dark">`; light/dark mode is handled by the stylesheet.
- Only put truly page-specific rules in an inline `<style>` (e.g. overriding chart colours `--c1..--c4` or canvas height).

## Classes
- Header: `.back` (link back to gallery), `.eyebrow` (date · field), `h1`, `.lede`, `.authors`
- Cards: `.card`; **Why it matters**: `<section class="card why"><h2>Why it matters</h2><p>…</p></section>` (blue card, required on every day page)
- Layout: `.grid` (2 columns, stacks on mobile)
- Sliders: `.controls` > `div` > `label` + `<output>` + `input[type=range]`; `.toggle` for checkboxes
- Plots: `canvas`, `.plot-title`, `.legend` (`<i>` swatches or `<span style="--k:var(--c1)">`)
- Stats: `.stats` > `.stat` > `.v` + `.l`
- Tables: plain `table`/`th`/`td` (numbers right-aligned)
- Text: `.note`, `.warn`, `code`, `.math` (monospace block), `.eq` (centred equation), `.cite` (citation block)
- Gallery (index.html): `.gallery` > `a.gallery-item` > `.date`, `.title`, `.summary`
- CSS variables for charts: `--accent`, `--muted`, `--grid`, `--line`, `--c1..--c4`, `--cx`
