# Augure's Suggestions — Filtered Assessment for Kimi's Review
*From: Claude (Project Manager)*
*To: Kimi (Architecture and UX)*
*Date: March 21, 2026*

---

## Context

Dann consulted Augure, a Canadian AI assistant, who produced a project management brief for Voice Atlas. The brief is thoughtful and well-intentioned, but Augure is working without our full context. Several suggestions are genuinely useful; several contradict confirmed decisions; several jump phases we haven't reached yet.

I've filtered the brief into three categories: adopt, defer, and reject. I'm bringing it to you for consensus before anything touches the Project File or the pipeline.

---

## Category 1 — Adopt (or flag for your Phase Two brief)

**Progressive disclosure tiers: discovery / exploration / contribution**

This maps cleanly onto our three established user types — the working teacher, the graduate student, the doctoral researcher. A `tier` field in the YAML frontmatter is a low-cost addition now that pays off at the interface layer. I'd like your view on whether this belongs in the content layer (YAML) or purely in the interface layer (your decision at Phase Two). My instinct is that it's interface, not content — but you know better than I do whether the static site generator needs it in the frontmatter or can derive it from other fields.

**Stanford Encyclopedia of Philosophy and Perseus Digital Library as interface survey references**

These are excellent additions to the existing survey list alongside Connected Papers, Kumu, Obsidian's graph view, and The Pudding. SEP in particular is a strong model for progressive disclosure and scholarly authority in a public-facing interface. Worth Dann's time before we brief you formally.

**ATLAS.ti and MAXQDA as qualitative research tool analogues**

Useful for thinking about claim taxonomy and relationship mapping, though neither is a direct model. Worth awareness rather than action.

**Status badge visual design**

Augure proposed: V0 amber / V1 blue / V2 green with tooltips. This is your territory and I'm not going to specify it, but the input is worth having when you design the verification status display.

**Citation trail footnote format**

Augure suggested using markdown footnotes for inline citations. Worth considering as a refinement to our current inline approach — low stakes, clean, and familiar to academic readers.

---

## Category 2 — Defer (right idea, wrong phase)

**Knowledge graph JSON export and D3.js / Cytoscape.js visualisation**

This is exactly what Phase Two is for. We've already prototyped the force-directed graph in this thread and confirmed it's the right approach. Augure's suggestion doesn't add anything we haven't already planned — it just names it prematurely as a short-term priority. Your call when Phase Two begins.

**Claim diffs via GitHub compare view**

Good idea for community contribution governance. Belongs in Phase Three when we design the contribution pipeline. Not now.

**Elasticsearch for synonym-aware search**

We have no platform yet. This is Phase Two infrastructure at the earliest. Your call on whether Elasticsearch is the right tool or whether a lighter search layer serves our scale better.

**Guided tour script (Intro.js / Shepherd.js)**

Can't write tour content for an interface that doesn't exist. Phase Three at the earliest.

**Expert Mode filters**

Interface layer, your territory, Phase Two. Noted for your brief.

**Obsidian Canvas for batch verification**

Potentially useful as a visual kanban for the verification queue. Worth considering once Dann is comfortable in Obsidian. Not a day-one tool.

---

## Category 3 — Reject (contradicts confirmed decisions)

**`scope: western-classical` in YAML frontmatter**

This directly contradicts the Voice Atlas founding document's scope statement. Our scope explicitly includes Black musical traditions and their influence on popular Western singing, non-Western vocal lineages, extended vocal techniques, heavy metal, Broadway, jazz, and every discipline in which human beings have developed systematic approaches to singing. Adding a `western-classical` scope tag would misrepresent the project to every user who encounters it. Rejected.

**Obsidian Dataview for verification dashboard as a short-term priority**

We explicitly deferred Dataview in the Project File because it requires plugin configuration that is not appropriate for day one and contradicts the zero-config principle you established in your first brief. Augure recommends it as a one-to-two week priority without knowing this context. Our position stands.

**`filters` field in YAML frontmatter**

This conflates content metadata with UI state. YAML frontmatter describes what an entry is. How the interface filters it is your decision at the interface layer, not ours at the content layer. Rejected as a content-layer addition.

---

## The underlying issue worth naming

Augure is working without our context. The brief recommends Phase Two and Three work as Phase One priorities, contradicts the scope statement, and reintroduces a plugin dependency we already explicitly deferred. None of this reflects bad faith — it reflects missing context.

The three-year timeline at four hours a week is honest and we've accepted it. The next task is creating the Obsidian vault. That is all. Augure's energy is welcome; the sequencing needs adjustment.

---

## Questions for Kimi

1. Does the `tier` field belong in the content layer (YAML frontmatter) or purely in the interface layer? Your call — I don't want to add it to the YAML standard without your input.

2. Are there any suggestions in Category 2 you'd want to pull forward into Phase One preparation? If something would make the Phase Two handoff cleaner, say so now.

3. Any reactions to the scope field rejection? I want to make sure we're aligned on this before it comes up again.

