---
marp: true
paginate: true
size: 16:9
title: "Façade-X Tutorial — From Practice to Standards"
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
    color: var(--ink); background: #fff;
    padding: 60px 70px; font-size: 26px; line-height: 1.5;
    border-top: 10px solid var(--navy);
  }
  h1, h2 { color: var(--navy); font-weight: 700; line-height: 1.15; }
  h2 { font-size: 1.6em; margin: 0 0 .6em; padding-bottom: .25em; border-bottom: 3px solid var(--accent); display: inline-block; }
  a { color: var(--navy-2); text-decoration: none; }
  strong { color: var(--navy); }
  footer { color: var(--muted); font-size: .55em; }
  section::after { color: var(--muted); font-size: .55em; }
  section.hero { background: linear-gradient(135deg, var(--navy) 0%, var(--navy-2) 100%); color: #fff; border-top: none; justify-content: center; }
  section.hero h1 { color: #fff; font-size: 2.1em; margin: 0 0 .2em; }
  section.hero p { color: #cfe0ee; }
  section.hero strong { color: #fff; }
  section.hero a { color: #fff; border-bottom: 1px solid var(--accent-2); }
  section.hero footer, section.hero::after { color: #cfe0ee; }
  .eyebrow { text-transform: uppercase; letter-spacing: .14em; font-size: .6em; font-weight: 600; color: var(--accent-2); margin: 0 0 .8em; }

  /* Cards */
  .cards { display: grid; grid-template-columns: repeat(3, 1fr); gap: 14px; margin-top: .4em; }
  .cards.two { grid-template-columns: 1fr 1fr; }
  .cards > div { background: var(--bg-soft); border: 1px solid var(--line); border-top: 4px solid var(--accent); border-radius: 8px; padding: .6em .8em; font-size: .6em; line-height: 1.4; }
  .cards > div b { color: var(--navy); font-size: 1.25em; display: block; margin-bottom: .3em; }
  .cards.research > div { border-top-color: var(--navy-2); }

  /* Timeline */
  .tl { display: flex; justify-content: space-between; position: relative; margin: 1.4em 0 .6em; font-size: .6em; }
  .tl::before { content: ""; position: absolute; top: 11px; left: 4%; right: 4%; height: 3px; background: var(--line); }
  .tl > div { position: relative; width: 15%; text-align: center; }
  .tl > div::before { content: ""; display: block; width: 18px; height: 18px; margin: 3px auto .5em; border-radius: 50%; background: var(--navy-2); border: 3px solid #fff; box-shadow: 0 0 0 2px var(--navy-2); }
  .tl > div.now::before { background: var(--accent); box-shadow: 0 0 0 2px var(--accent); }
  .tl b { display: block; color: var(--navy); font-size: 1.2em; }

  /* Spec stack */
  .stack { display: grid; grid-template-columns: repeat(4, 1fr); gap: 10px; font-size: .6em; margin-top: .4em; }
  .stack > div { border: 2px solid var(--navy-2); background: #e8f0f7; border-radius: 8px; padding: .5em .7em; }
  .stack > div b { color: var(--navy); display: block; }
  .stack .wide { grid-column: span 4; text-align: center; }
  .stack .half { grid-column: span 2; }
  .pill { display: inline-block; font-size: .8em; padding: .05em .6em; border-radius: 1em; margin-top: .3em; }
  .pill.ok { background: #dff3e4; color: #1e7b3a; }
  .pill.wip { background: #fdf1ea; color: #b34d1c; }

  .q { font-size: .95em; }
  .q li { margin: .45em 0; }
  .links { font-size: .75em; }
---

<!-- _class: hero -->
<!-- _paginate: false -->

<p class="eyebrow">Slot 3 · From Practice to Standards</p>

# The W3C Data Façades Community Group

What we are standardising, and what comes next: the research agenda and the engineering agenda.

<!--
17:40. ~10 min talk, ~10 min discussion.
-->

---

## How we got here

<div class="tl">
  <div><b>2021</b>Façade-X idea + SPARQL Anything<br><i>SEMANTiCS</i></div>
  <div><b>2022</b>Materialisation approaches<br><i>Semantic Web J.</i></div>
  <div><b>2023</b>The KGC method<br><i>ACM TOIT</i></div>
  <div><b>2025</b>W3C Data Façades CG</div>
  <div><b>2026</b>Theory of Façade-X data access<br><i>TGDK</i></div>
  <div class="now"><b>Oct 2026</b>SPARQL Anything v1.3.0<br>Specs release 0.1</div>
</div>

From one paper and one engine to **a community, several implementations, and a draft standard**.

<!--
~45 s. Today's afternoon showed the community side: production (Triply, railways, procurement), teaching.
-->

---

## Why a standard?

<div class="cards">
  <div><b>More than one engine</b>Façade-X is now implemented beyond SPARQL Anything. The same query should give the same answer everywhere.</div>
  <div><b>Shared semantics</b>What does a CSV, a JSON number, an XML attribute become? Today the answer is "what the engine does".</div>
  <div><b>Trust for adopters</b>A stable, versioned reference lowers the risk of building on the approach.</div>
</div>

<!--
~1 min. The key word is interoperability: queries portable across engines.
-->

---

## What the CG is writing

<div class="stack">
  <div class="wide"><b>Model</b>containers, slots, values <span class="pill ok">0.1</span></div>
  <div class="half"><b>Schema vocabulary</b><code>fx:</code> terms used in the façade <span class="pill ok">0.1</span></div>
  <div class="half"><b>Engine vocabulary</b><code>fxe:</code> options, e.g. <code>fxe:csv.headers</code> <span class="pill ok">0.1</span></div>
  <div><b>CSV</b> mapping <span class="pill ok">0.1</span></div>
  <div><b>JSON</b> mapping <span class="pill ok">0.1</span></div>
  <div><b>XML</b> mapping <span class="pill ok">0.1</span></div>
  <div><b>Design</b> principles <span class="pill wip">in progress</span></div>
  <div class="half"><b>SPARQL data access</b>how a query reaches a façade <span class="pill ok">0.1</span></div>
  <div class="half"><b>HTTP / protocol access</b>remote resources, APIs <span class="pill wip">in progress</span></div>
  <div class="wide" style="background:#fff;border-style:dashed"><b>Primer</b> · <b>Test suite</b>: input files and expected RDF, per format</div>
</div>

<!--
~1.5 min. Bottom-up: model, vocabularies, one mapping per format, access. The test suite makes it checkable.
Check the 0.1 pills against the actual release contents before the day.
-->

---

## How we work

<div class="cards">
  <div><b>In the open</b>Specs, issues and meeting minutes on GitHub. Anyone can read and comment.</div>
  <div><b>Issue-driven</b>Each design decision is an issue: discussed in meetings, recorded in the spec.</div>
  <div><b>Versioned releases</b>A latest release, a working draft, and frozen snapshots per version.</div>
</div>

<!--
~45 s. Example of a decision: typing principle, keep the lexical form, use the natural XSD datatype (JSON numbers → xsd:decimal, as in the intro).
-->

---

## The research agenda

<div class="cards research">
  <div><b>Theory beyond BGPs</b>Satisfiability is settled for basic graph patterns. Next: full SPARQL, and using it to prune and optimise.</div>
  <div><b>Large data, small memory</b>Evaluate queries over big files as streams, without loading the whole façade.</div>
  <div><b>Federation</b>Plan and optimise queries that join many façades and remote sources.</div>
  <div><b>Types and entailment</b>Should <code>1775</code> match <code>"1775"^^xsd:decimal</code>? Term equality vs value-based matching.</div>
  <div><b>Expressive power</b>Beyond context-free formats: what can, and should, a façade represent?</div>
  <div><b>Façades and LLMs</b>One uniform shape for any source: a target for query generation and KG pipelines.</div>
</div>

<!--
~1.5 min. Each card is an open question; several are open to collaboration.
-->

---

## The engineering agenda: frameworks we need

<div class="cards">
  <div><b>Conformance</b>A shared test suite and a runner: any engine can check itself against the spec.</div>
  <div><b>More engines</b>Façade-X inside more SPARQL engines and KG platforms, not only as a separate tool.</div>
  <div><b>More formats</b>New mappings, shared across engines rather than re-invented in each.</div>
  <div><b>Developer tooling</b>Editors, query debugging, inspecting a façade, validating it with SHACL.</div>
  <div><b>Pipelines</b>Façade queries as reusable steps in ELT and data-space workflows.</div>
  <div><b>A cookbook</b>Good practices and patterns, from the people who use it in production and teaching.</div>
</div>

<!--
~1.5 min. This is where implementers and practitioners in the room can help most.
-->

---

## Get involved

<div class="cards two">
  <div><b>Join the CG</b>Free, open to anyone with a W3C account.<br><a href="https://www.w3.org/community/facade-x/">w3.org/community/facade-x</a></div>
  <div><b>Contribute</b>Comment on issues, propose a format mapping, add tests, report how you use it.<br><a href="https://github.com/w3c-facade-x">github.com/w3c-facade-x</a></div>
  <div><b>Use and implement</b>Build on SPARQL Anything, or implement Façade-X in your engine.<br><a href="https://sparql-anything.cc">sparql-anything.cc</a></div>
  <div><b>Teach it</b>Reuse today's notebooks and slides in your courses.<br><a href="https://w3c-facade-x.github.io/iswc2026-tutorial">w3c-facade-x.github.io/iswc2026-tutorial</a></div>
</div>

<!--
~30 s.
-->

---

## Discussion

<ol class="q">
  <li>Which <strong>formats</strong> matter most to you, and which are missing?</li>
  <li>What would stop you from <strong>adopting</strong> Façade-X in your work?</li>
  <li>Would you <strong>implement</strong> it in your engine or platform? What would you need?</li>
  <li>Which item of the <strong>research agenda</strong> should come first?</li>
</ol>

<!--
~10 min. Start from Q1 to get hands up; take notes for the CG minutes.
-->

---

<!-- _class: hero -->
<!-- _paginate: false -->

<p class="eyebrow">Thank you</p>

# Join us

**W3C CG** · <a href="https://www.w3.org/community/facade-x/">w3.org/community/facade-x</a>
**Specs** · <a href="https://github.com/w3c-facade-x">github.com/w3c-facade-x</a>
**SPARQL Anything** · <a href="https://sparql-anything.cc">sparql-anything.cc</a>
**Tutorial** · <a href="https://w3c-facade-x.github.io/iswc2026-tutorial">w3c-facade-x.github.io/iswc2026-tutorial</a>
