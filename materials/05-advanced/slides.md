---
marp: true
paginate: true
size: 16:9
title: "Façade-X Tutorial — Introduction"
footer: "Façade-X Tutorial · ISWC 2026 · Bari"
style: |
  :root {
    --navy: #023558;
    --navy-2: #0a4a76;
    --accent: #e8703a;
    --accent-2: #f2a154;
    --ink: #1c2530;
    --muted: #5b6b7a;
    --line: #e2e8ee;
    --bg-soft: #f5f8fb;
  }
  section {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    color: var(--ink);
    background: #fff;
    padding: 60px 70px;
    font-size: 26px;
    line-height: 1.5;
    border-top: 10px solid var(--navy);
  }
  h1, h2 { color: var(--navy); font-weight: 700; line-height: 1.15; }
  h2 { font-size: 1.6em; margin: 0 0 .6em; padding-bottom: .25em; border-bottom: 3px solid var(--accent); display: inline-block; }
  a { color: var(--navy-2); text-decoration: none; }
  strong { color: var(--navy); }
  footer { color: var(--muted); font-size: .55em; }
  section::after { color: var(--muted); font-size: .55em; }

  /* Hero (title / closing) */
  section.hero {
    background: linear-gradient(135deg, var(--navy) 0%, var(--navy-2) 100%);
    color: #fff;
    border-top: none;
    justify-content: center;
  }
  section.hero h1 { color: #fff; font-size: 2.1em; margin: 0 0 .2em; }
  section.hero h2 { color: #fff; border-bottom-color: var(--accent-2); }
  section.hero p { color: #cfe0ee; }
  section.hero strong { color: #fff; }
  section.hero footer, section.hero::after { color: #cfe0ee; }
  .eyebrow {
    text-transform: uppercase; letter-spacing: .14em;
    font-size: .6em; font-weight: 600; color: var(--accent-2);
    margin: 0 0 .8em;
  }
  .meta { font-size: .75em; color: #e6eef5; margin-top: 1.4em; }
  .badges { margin-top: 1em; }
  .badge {
    display: inline-block; margin: 0 .35em .35em 0;
    background: rgba(255,255,255,.12); border: 1px solid rgba(255,255,255,.25);
    color: #fff; padding: .2em .8em; border-radius: 1em; font-size: .55em;
  }

  /* Agenda table */
  table { border-collapse: collapse; width: 100%; font-size: .68em; }
  th { background: var(--navy); color: #fff; text-align: left; padding: .45em .7em; }
  section table th strong {color: #fff}
  td { padding: .35em .7em; border-bottom: 1px solid var(--line); }
  tr.slot td { background: var(--bg-soft); color: var(--navy); font-weight: 700; }
  tr.break td { background: #fdf1ea; color: var(--accent); font-weight: 600; }
  td.who { color: var(--muted); white-space: nowrap; }

  /* Presenter cards */
  .people { display: grid; grid-template-columns: repeat(3, 1fr); gap: 18px; margin-top: .4em; }
  .card {
    background: var(--bg-soft); border: 1px solid var(--line);
    border-left: 5px solid var(--accent); border-radius: 8px;
    padding: .55em .8em; font-size: .62em; line-height: 1.35;
  }
  .card b { color: var(--navy); font-size: 1.2em; display: block; }
  .card .aff { color: var(--muted); display: block; margin-bottom: .3em; }
---

<!-- _class: hero -->
<!-- _paginate: false -->

<p class="eyebrow">ISWC 2026 · Half-Day Tutorial</p>

# Façade-X: Querying Any Format as a Knowledge Graph

Session 5: Guided Excercises

<div class="meta">📍 Bari, Italy &nbsp;·&nbsp; 📅 25 October 2026 &nbsp;·&nbsp; ⏱️ 14:10–18:00</div>

<div class="badges"><span class="badge">SPARQL</span><span class="badge">Knowledge Graphs</span><span class="badge">Data Integration</span><span class="badge">Hands-on</span></div>

<!--
Welcome. Organised by the W3C Data Façades Community Group.
-->

---

## Two notebooks: pick one

Both cover the same basics: CLI and Python, CSV → KG (`csv.headers`, `fx:entity`), templates (`?_`, `-v`, `-p`), reuse (`-l`, `query=`).
They differ in the features they touch:

| | **Tate** | **Nobel** |
|---|---|---|
| Sources | Local files: CSV, JSON, Markdown | Local CSV + live JSON API |
| Remote data | A JSON file on the Web | An HTTP API: `media-type`, `http.query.*` |
| Many sources | A folder as a source: `archive.matches`, nested `SERVICE` | Paging an API: `limit`/`offset`, `VALUES`, `http.sleep` |
| Large data | Slicing ~69,000 rows: `slice`, `-st` | — |
| Text | A Markdown file as document or as text: `txt.regex` | Values inside JSON as text: nested `SERVICE`, `txt.split`, `txt.regex` + `txt.group` |

<div style="display:flex; justify-content:space-around; font-size:1.1em; font-weight:700; margin-top:.6em">
  <span>Tate · <a href="https://bit.ly/fx-tutorial-adv">bit.ly/fx-tutorial-adv</a></span>
  <span>Nobel · <a href="https://bit.ly/fx-tutorial-adv2">bit.ly/fx-tutorial-adv2</a></span>
</div>

**✋ Show of hands: files and scale (Tate) or APIs and HTTP (Nobel)?**