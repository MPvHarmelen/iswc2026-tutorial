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

- The Façade-X idea and its foundations
- Hands-on with SPARQL Anything
- (coffee break)
- How it is used in practice, taught, and standardised

<!--
~30 s. Keep it flat: what this afternoon is for.
-->


---

## Agenda

<table>
<tr><th>Time</th><th>Session</th><th>Who</th></tr>
<tr class="slot"><td>14:10–14:50</td><td colspan="2">Slot 1 · The Problem and the Idea</td></tr>
<tr><td>14:10–14:30</td><td>Introduction to Façade-X</td><td class="who">Enrico</td></tr>
<tr><td>14:30–14:50</td><td>Foundations: towards a theory of façade-based data access</td><td class="who">Luigi</td></tr>
<tr class="slot"><td>14:50–16:10</td><td colspan="2">Slot 2 · Hands-on with SPARQL Anything</td></tr>
<tr><td>14:50–15:20</td><td>Live querying of CSV, JSON and XML</td><td class="who">Luigi</td></tr>
<tr><td>15:20–15:45</td><td>Functions and magic properties</td><td class="who">Luigi</td></tr>
<tr><td>15:45–16:10</td><td>Guided exercises with real datasets</td><td class="who">Enrico</td></tr>
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
<div class="card"><b>Enrico Daga</b><span class="aff">KMi, The Open University (UK)</span>Co-founder of SPARQL Anything · chair, W3C Data Façades CG</div>
<div class="card"><b>Martin van Harmelen</b><span class="aff">Triply (NL)</span>SPARQL engine design and ELT pipelines on TriplyDB</div>
<div class="card"><b>Mathias Vanden Auweele</b><span class="aff">MATDATA (BE)</span>Railway infrastructure data and production KGs</div>
<div class="card"><b>Ryan Shaw</b><span class="aff">UNC Chapel Hill (US)</span>Teaches KG management with SPARQL Anything</div>
<div class="card"><b>Ivo Velitchkov</b><span class="aff">Kvistgaard (DK)</span>Consultant and trainer in semantic technologies</div>
</div>

<!--
~1.5 min. Each presenter stands up / waves; one sentence each.
-->

---

## Show of hands ✋

<style scoped>
ol { font-size: .95em; }
ol li { margin: .35em 0; }
.aside { color: var(--muted); font-size: .7em; margin-top: 1em; }
</style>

Raise your hand if you…

1. have **heard of** Façade-X or SPARQL Anything before today
2. have **tried** SPARQL Anything, even once
3. **use** it in your work: research, a project, a product, teaching
4. have built a knowledge graph from CSV, JSON or XML **some other way**: RML/YARRRML, SPARQL Generate, scripts…

<p class="aside">And: what data gives you the most trouble? Keep it for the clinic.</p>

<!--
~1.5 min. Keep hands up and lower them step by step: 1 → 2 → 3.
Q1 low: spend more time on the idea in the intro.
Q3 high: ask one or two people what they use it for.
Q4 high: the comparison with mapping languages will land; mention it explicitly.
-->

---

## What you will learn today

<style scoped>
.cols { display: grid; grid-template-columns: 1fr 1fr; gap: 28px; margin-top: .3em; }
.col h3 { color: var(--accent); font-size: .8em; text-transform: uppercase; letter-spacing: .1em; margin: 0 0 .4em; }
.col ul { font-size: .78em; margin: 0; padding-left: 1.1em; }
.col li { margin: .35em 0; }
</style>

<div class="cols">
<div class="col">

### In practice

- Query **CSV, JSON, XML, Markdown, APIs** as a knowledge graph, with SPARQL alone
- Map any source to **your own vocabulary** in one `CONSTRUCT`
- **Join formats** in a single query
- Turn queries into **pipelines**: templates, parameters, reuse
- Use **SPARQL Anything** from the command line and from Python

</div>
<div class="col">

### Beyond practice

- The **Façade-X idea**: one minimal model (containers, slots, values) for any format
- Its **theory**: what we can know about a query before touching the data
- How it is **deployed** in production: railways, procurement, TriplyDB
- How it is **taught** in KG courses
- How it is becoming a **standard**, and how to join the W3C CG

</div>
</div>

<!--
~1 min. Left column: what you take home and use on Monday.
Right column: why it works, where it is used, where it is going.
-->

---

## Before we start

- **SPARQL Anything** downloaded, or **PySPARQL Anything** in Python / Jupyter
- No local setup? A **Google Colab** notebook is available
- Slides, notebooks and exercises: **w3c-facade-x.github.io/iswc2026-tutorial**
- Questions any time — and keep your own data for the clinic during the coffee break.

<!--
~1 min. Check who has the tool running; point to Colab fallback.
-->

---

<!-- _class: hero -->
<!-- _paginate: false -->

<p class="eyebrow">Slot 1 · The Problem and the Idea</p>

# Let's start.

**w3c-facade-x.github.io/iswc2026-tutorial**

---

## Building a knowledge graph

<style scoped>
.flow { display: flex; align-items: center; justify-content: space-between; margin: 1em 0 1.2em; font-size: .8em; }
.step { background: var(--bg-soft); border: 1px solid var(--line); border-top: 4px solid var(--navy); border-radius: 8px; padding: .5em .8em; text-align: center; width: 17%; }
.step.hot { border-top-color: var(--accent); }
.arrow { color: var(--muted); }
</style>

<div class="flow">
<div class="step"><b>Sources</b><br>CSV, JSON, XML, DBs, APIs</div><span class="arrow">→</span>
<div class="step"><b>Ontology</b><br>reuse or design</div><span class="arrow">→</span>
<div class="step hot"><b>Mapping</b><br>source → ontology</div><span class="arrow">→</span>
<div class="step"><b>Execution</b><br>materialise or virtualise</div><span class="arrow">→</span>
<div class="step"><b>KG</b><br>validate, publish, query</div>
</div>

Every method has these steps. The **mapping** is where most of the effort goes, and where the source formats get in the way.

<!--
~1 min. Standard KGC methodology. Point at the orange box: this is what the afternoon is about.
-->

---

## Mapping today

- **One language per kind of source**: R2RML for databases, RML/YARRRML for files, XSPARQL for XML, SPARQL Generate…
- **A second language next to SPARQL**, with its own syntax, tools and debugging
- The mapping must **know the format**: JSONPath, XPath, column names, iterators
- Often the real answer is **a script** in Python or Java

The people who know the data are not always the people who can write the mapping.

<!--
~1 min. Not an attack on mapping languages: they work. The point is cost: format-specific knowledge + an extra language.
Callback to show-of-hands Q4 if many hands went up.
-->

---

## The Façade-X idea

**Don't map the format. Look at every format through the same façade, then map with SPARQL.**

1. **Façade**: any source is seen as RDF with *one* generic structure, whatever its format
2. **Mapping**: a SPARQL `CONSTRUCT` from that structure to your ontology

The format-specific work moves into the engine. You only write SPARQL.

<!--
~1 min. The core message of the tutorial. "Façade" = a generic view over the source, built by the engine.
-->

---

## The meta-model: containers, slots, values

| | What it is | In RDF |
|---|---|---|
| **Container** | anything that holds things: a file, a row, an object, an array, an element | a node (blank by default); the top one is `fx:root` |
| **Slot** | a position in a container, by **number** or by **name** | `rdf:_1`, `rdf:_2`… · `xyz:name`, `xyz:born`… |
| **Value** | the data | a literal |
| **Type** | an optional label of a container | `rdf:type`, e.g. an XML element name |

That's all. No CSV-, JSON- or XML-specific vocabulary.

<!--
~1.5 min. Four notions. Numbered slots = order (rows, arrays, children). Named slots = keys, headers, attributes.
-->

---

## Same data, same façade

<style scoped>
.three { display: grid; grid-template-columns: 1fr 1fr 1fr; gap: 16px; font-size: .55em; }
.three pre { margin: .3em 0; }
.three b { color: var(--navy); }
</style>

<div class="three">
<div>

<b>CSV</b> (with headers)
```
name,born
Turner,1775
```
```turtle
[] a fx:root ;
  rdf:_1 [
    xyz:name "Turner" ;
    xyz:born "1775" ] .
```

</div>
<div>

<b>JSON</b>
```json
[ {"name": "Turner",
   "born": 1775} ]
```
```turtle
[] a fx:root ;
  rdf:_1 [
    xyz:name "Turner" ;
    xyz:born 1775 ] .
```

</div>
<div>

<b>XML</b>
```xml
<artists>
  <artist born="1775">Turner</artist>
</artists>
```
```turtle
[] a fx:root, xyz:artists ;
  rdf:_1 [ a xyz:artist ;
    xyz:born "1775" ;
    rdf:_1 "Turner" ] .
```

</div>
</div>

Three formats, one shape. Only the details differ: a JSON number stays a number, an XML element keeps its name as a type.

<!--
~2 min. Let them spot the similarities first. Then the two differences: datatypes, types.
-->

---

## From the façade to your knowledge graph

```sparql
CONSTRUCT {
  ?artist a schema:Person ; schema:name ?name ; schema:birthDate ?born .
} WHERE {
  SERVICE <x-sparql-anything:location=artists.csv,csv.headers=true> {
    ?row xyz:name ?name ; xyz:born ?born .
  }
  BIND (fx:entity(ex:, ?name) AS ?artist)
}
```

- `SERVICE <x-sparql-anything:…>` builds the façade of the source, on the fly
- Change `artists.csv` to `artists.json`: **the same query still works**
- Options in the IRI (or in the query) tune the façade: headers, delimiters, HTTP, slicing…

<!--
~1.5 min. Prefixes omitted. The punchline is the second bullet.
-->

---

## Why "opinionated"

- **Minimal on purpose**: four notions, so users learn one model, not one per format
- **SPARQL only**: no second language; joins, filters, functions come for free
- **Format-agnostic queries**: the shape of the data matters, not its syntax
- **Virtual or materialised**: query sources directly, or save the result as RDF
- The price: some format details are left out, by design

<!--
~1 min. Be honest about the trade-off in the last bullet.
-->

---

## What comes next

- **Luigi**: what can we know about a query over a façade, before touching the data?
- **Hands-on**: SPARQL Anything on CSV, JSON, XML, and the guided exercises
- **After the break**: Façade-X in production, in teaching, and in the W3C CG

<!--
~15 s. Hand over to Luigi.
-->