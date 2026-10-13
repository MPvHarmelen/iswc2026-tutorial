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

## The afternoon in one line

**Any data format → a knowledge graph → SPARQL alone.**

- The idea and its foundations
- Hands-on with SPARQL Anything
- How it is used in practice, taught, and standardised

<!--
~30 s. Keep it flat: what this afternoon is for.
-->

---

## Agenda

<table>
<tr><th>Time</th><th>Session</th><th>Who</th></tr>
<tr class="slot"><td>14:10–14:50</td><td colspan="2">Slot 1 · The Problem and the Idea</td></tr>
<tr><td>14:10–14:30</td><td>Introduction to Façade-X</td><td class="who">Enrico &amp; Luigi</td></tr>
<tr><td>14:30–14:50</td><td>Foundations: towards a theory of façade-based data access</td><td class="who">Enrico &amp; Luigi</td></tr>
<tr class="slot"><td>14:50–16:10</td><td colspan="2">Slot 2 · Hands-on with SPARQL Anything</td></tr>
<tr><td>14:50–15:20</td><td>Live querying of CSV, JSON and XML</td><td class="who">Luigi</td></tr>
<tr><td>15:20–15:45</td><td>Functions and magic properties</td><td class="who">Enrico</td></tr>
<tr><td>15:45–16:10</td><td>Guided exercises with real datasets</td><td class="who">Enrico &amp; Luigi</td></tr>
<tr class="break"><td>16:10–16:30</td><td>Break · SPARQL Anything Clinic — bring your data</td><td class="who">All</td></tr>
<tr class="slot"><td>16:30–18:00</td><td colspan="2">Slot 3 · From Practice to Standards</td></tr>
<tr><td>16:30–17:30</td><td>Industry talks: railway KG · TriplyDB deployment · Public Procurement Data Space</td><td class="who">Mathias, Martin, Ivo</td></tr>
<tr><td>17:30–17:40</td><td>Teaching KG management with SPARQL Anything</td><td class="who">Ryan</td></tr>
<tr><td>17:40–18:00</td><td>W3C Data Façades CG: roadmap and discussion</td><td class="who">Enrico</td></tr>
</table>

<!--
~1 min. Point at the three slots; the break doubles as a clinic.
-->

---

## Presenters

<div class="people">
<div class="card"><b>Luigi Asprino</b><span class="aff">Università Telematica San Raffaele, Roma (IT)</span>Co-founder of SPARQL Anything · chair, W3C Data Façades CG</div>
<div class="card"><b>Enrico Daga</b><span class="aff">KMi, The Open University (UK)</span>Co-founder of SPARQL Anything · KG construction for cultural heritage</div>
<div class="card"><b>Martin van Harmelen</b><span class="aff">Triply (NL)</span>SPARQL engine design and ELT pipelines on TriplyDB</div>
<div class="card"><b>Mathias Vanden Auweele</b><span class="aff">MATDATA (BE)</span>Railway infrastructure data and production KGs</div>
<div class="card"><b>Ryan Shaw</b><span class="aff">UNC Chapel Hill (US)</span>Teaches KG management with SPARQL Anything</div>
<div class="card"><b>Ivo Velitchkov</b><span class="aff">Kvistgaard (DK)</span>Consultant and trainer in semantic technologies</div>
</div>

<!--
~1.5 min. Each presenter stands up / waves; one sentence each.
-->

---

## Before we start

- **SPARQL Anything** downloaded, or **PySPARQL Anything** in Python / Jupyter
- No local setup? A **Google Colab** notebook is available
- Slides, notebooks and exercises: **w3c-facade-x.github.io/iswc2026-tutorial**
- Questions any time — and keep your own data for the clinic at 16:10

<!--
~1 min. Check who has the tool running; point to Colab fallback.
-->

---

<!-- _class: hero -->
<!-- _paginate: false -->

<p class="eyebrow">Slot 1 · The Problem and the Idea</p>

# Let's start.

**w3c-facade-x.github.io/iswc2026-tutorial**