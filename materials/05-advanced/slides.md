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

Integrate CSV, JSON, XML, spreadsheets and more using SPARQL alone.

<div class="meta">📍 Bari, Italy &nbsp;·&nbsp; 📅 25 October 2026 &nbsp;·&nbsp; ⏱️ 14:10–18:00</div>

<div class="badges"><span class="badge">SPARQL</span><span class="badge">Knowledge Graphs</span><span class="badge">Data Integration</span><span class="badge">Hands-on</span></div>

<!--
Welcome. Organised by the W3C Data Façades Community Group.
-->

---

# FX ISWC Tutorial - Hands-on with SPARQL Anything: guided exercises

In these exercises you build data integration pipelines with the **SPARQL Anything command line interface (CLI)**, using real data from the [Tate collection](https://github.com/tategallery/collection): artists and artworks published as CSV, JSON and Markdown (CC0).

Each step is shown twice: as a terminal command (`!java -jar …`) and with [PySPARQL Anything](https://github.com/SPARQL-Anything/PySPARQL-Anything), the Python library that runs the same engine.

**You need:** a Google account to run the notebook in Colab, and basic SPARQL (`SELECT`, `CONSTRUCT`, `SERVICE`). Nothing to install on your machine.

---

<style>
.flex-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 200px; /* Set a height for the container */
}
</style>
<div class="flex-container">

![width:400px](fx-tutorial-adv.png)

</div>

---

## Exercises

| # | Exercise | You will learn to… | Key features |
|---|---|---|---|
| 0 | Install the CLI | run SPARQL Anything from a single jar, and from Python | `-q`, `-f`, `fxe:content` |
| 1 | From a CSV file to a knowledge graph | see how Façade-X represents a table, and map it to your own vocabulary | `csv.headers`, `csv.null-string`, `fx:cardinal`, `fx:entity`, `-o` |
| 2 | Two formats, one query | join JSON from the Web with a local CSV in a single query | `rdfs:member`, remote `location`, datatypes in joins |
| 3 | From a query to a pipeline | turn a query into a template and run it once per row of a result set | `?_` parameters, `-v`, `-p` |
| 4 | A folder as a data source | query every file in a folder with one query | folders, `archive.matches`, nested `SERVICE` |
| 5 | Reuse what you built | query the RDF you produced and use a saved query as a source | `-l`, `query=` |
| 6 | Scaling up | convert ~69,000 rows with limited memory, and turn the graph back into a table | `slice`, `-st`, `-f CSV` |
| 7 | Documents and text | read the same file as a structured document or as plain text | Markdown, `media-type`, `txt.regex` |

Exercises **0–3** are the core (about 30 minutes). Exercises **4–7** go further (another 30 minutes).

--

## The notebook: **https://bit.ly/fx-tutorial-adv**

- Run the cells in order: later exercises reuse files created earlier.
- `%%writefile` cells save a query to a file; the cells after them run it.
- Cells marked `# YOUR CODE HERE` are for you to try.
- To change the SPARQL Anything version, edit the download URL in exercise 0.
- Reference documentation: [sparql-anything.cc](https://sparql-anything.cc)

