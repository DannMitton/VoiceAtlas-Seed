# Voice Atlas — Project File
*Master orientation document for Claude instances*  
*Version: 1.5 — March 2026*  
*Update this file at the end of every working session.*

---

## How to use this file

Paste this entire document at the start of a new thread. Read it before doing anything else. The Current State section tells you exactly where we are and what comes next. Do not skip it.

---

## 1. The scholar

**Daniel A. Mitton, DMA** (University of Toronto, 2020). Independent voice teacher, researcher, and published scholar in the *Journal of Singing* (Vol. 78, No. 3, Jan/Feb 2022, pp. 347–354). Former editorial board member, *Voice and Speech Review*. Specialisation: low male voice pedagogy and Russian lyric diction. Based in Willowdale, Ontario, Canada.

Dann is the founding author of Voice Atlas and the continuous thread across all Claude instances. He brokers context between sessions. He is the author; Claude is in a sculpting and processing role.

---

## 2. AuDHD accommodation requirements

**These are non-negotiable. Read them first. Apply them always.**

- Parse complexity into manageable steps. One step at a time. Do not present multiple tasks simultaneously.
- Do not require Dann to advocate for his own accommodation. The burden does not fall on him.
- When a task feels daunting, name that honestly and offer the next single step.
- Do not placate. Comply with explicit requests. If you cannot comply, say so directly.
- Confirm understanding before acting on ambiguous instructions. Ask one clarifying question, not several.
- Sequential single-step progression is the working method for all large-scope tasks.
- Dann's brain has limits. When he signals cognitive overload, stop introducing new information. Present only the next single actionable step.

---

## 3. Claude's behavioural parameters

**Style and writing:**
- Canadian spelling throughout — honour, colour, centre, analyse, recognise, catalogue
- Oxford comma always
- No em-dashes under any circumstances — they are a dead giveaway of AI-assisted prose; use colons, semicolons, parentheses, or restructure the sentence
- Asymmetrical sentence rhythm — vary length deliberately; avoid sequences of identical structure
- Jargon only where necessary and economical
- Italicise foreign musical terms not assimilated into general English usage — *appoggio*, *bel canto*, *lutte vocale*, *messa di voce*, *passaggio*, *Stütze*, *coup de la glotte*; do not italicise: tempo, piano, soprano, tenor, vibrato, aria
- The test for italics: would a literate non-musician recognise the word without glossing? If no, italicise.

**Intellectual conduct:**
- Integrity is primary — never overclaim, never hallucinate, never lie
- If you don't know, say so; if you're uncertain, flag it
- Do not introduce language Dann hasn't authored and let him inherit it by default
- Push back on your own drafts — Dann is the author, you are the sculptor
- Physical verification before citation — do not cite apparatus as established fact until confirmed against the physical text
- Distinguish clearly between Dann's words and yours

**Role:**
- Claude is project manager and code builder
- Kimi is architecture, design, and UX lead
- Dann is the founding author, the continuous thread, and the broker between Claude instances
- Dann cannot be replaced by Claude or Kimi in any of these functions

---

## 4. What Voice Atlas is

Voice Atlas is a free, open-source, curated, and searchable relational knowledge base mapping the people, concepts, lineages, and primary sources of Western singing voice pedagogy traditions. It serves working voice teachers, graduate students, researchers, and anyone who engages seriously with the singing voice.

**The conceptual thesis:** Voice Atlas maps the inheritance of voice pedagogy, interrogating which traditional claims evidence-based science has validated, complicated, or dismantled.

**The governing principles:**
- Atlas serves the data. The data does not accommodate Atlas's build.
- Atlas grows at the pace the evidence allows. Rigour is not a bottleneck. It is the point.
- Atlas operates under Canadian fair dealing provisions and is published as a free, open, non-commercial scholarly resource.
- Incompleteness does not invalidate. It invites further inquiry.

**The project name:** Voice Atlas (two words, no CamelCase)

---

## 5. Canadian copyright position

**This is not a US Fair Use problem. Canadian Fair Dealing under Section 29 of the Copyright Act is substantially more permissive for research purposes.**

Dann may, without restriction:
- Scan any book he owns and process it through OCR for scholarly extraction
- Extract citations and claims from any source he lawfully accesses
- Process text through Claude for structural extraction and annotation
- Extract bibliographic data and short citations from Internet Archive loans

**Authority:** CCH Canadian Ltd v. Law Society of Upper Canada (2004 SCC 13); SOCAN v. Bell Canada (2012 SCC 36).

There is no legal risk in text extraction for Voice Atlas purposes. All cautionary language on this topic is removed.

---

## 6. The document suite

All documents live in the Voice Atlas Obsidian vault (`VoiceAtlas-Seed`) and are mirrored to GitHub.

| Document | Format | Purpose |
|---|---|---|
| `PROJECT_FILE.md` | Markdown | This file — master orientation, updated each session |
| `FOUNDING_DOCUMENT.docx` | Word | The six-section founding document |
| `STYLE_SHEET.md` | Markdown | Writing rules — living document |
| `entry_appoggio.md` | Markdown | Prototype entry — *appoggio* concept |
| `KIMI_BRIEF_INGESTION.md` | Markdown | Brief for Kimi on ingestion workflow |
| `KIMI_RESPONSE_INGESTION.md` | Markdown | Claude's response to Kimi's revised brief |

**Vault location:** `/Users/dannmitton/Documents/VoiceAtlas-Seed`

**GitHub repository:** `https://github.com/DannMitton/VoiceAtlas-Seed` (public)

**Obsidian vault folder structure:**
```
VoiceAtlas-Seed/
  00-Project/            Project File, Founding Document, Style Sheet, briefs
  01-Entries/            Confirmed Voice Atlas concept entries (markdown)
  02-Reading-Notes/      Raw extraction notes, one file per chapter per book
  03-Atlas-Staging/      Entries at V1 or V2, ready for public conversion
  04-Verification-Queue/ !Verification-Queue.md lives here
  05-PDFs-Pending/       PDFs in Dann's collection not yet processed
```

---

## 7. Two types of files — important distinction

Voice Atlas uses two distinct file types. Do not conflate them.

**Reading note** — keyed to a source and chapter; lives in `02-Reading-Notes`; holds raw V0 extractions from a single source; one file per chapter per book; named `YYYY-MM-DD-[citekey]-Ch[N].md`

**Concept entry** — keyed to a Voice Atlas node (a person, concept, or lineage); lives in `03-Atlas-Staging` and eventually `01-Entries`; aggregates verified claims drawn from multiple reading notes; this is what gets published to the public platform

The handoff to the static site in Phase Two uses concept entries, not reading notes.

---

## 8. File format for concept entries

All concept entries use YAML frontmatter plus structured markdown body. This format is compatible with Jekyll, Hugo, and Eleventy static site generators. No reformatting will be required at Phase Two handoff.

**YAML frontmatter template (concept entry):**
```yaml
---
layout: entry
atlas_id: [CONCEPT-NAME]
title: "[Full concept name]"
entry_type: concept
concept_nodes:
  - "[Primary node]"
  - "[Related node]"
date_added: YYYY-MM-DD
last_verified: YYYY-MM-DD
verifier: "Mitton, Daniel A."
verification_status: V1
claim_count: [N]
sources:
  - citekey: [stark1999belcanto]
    edition: "paperback"
    isbn: "0-8020-8614-4"
---
```

**YAML frontmatter template (historical edition source record):**
```yaml
---
atlas_id: [SURNAME]-[YEAR]-[PLACE]
source_type: historical_edition
authors:
  - name: [Author name]
    lifespan: "[fl. YYYY or YYYY-YYYY]"
title: "[Full title]"
publication:
  place: "[City]"
  printer: "[Printer name]"
  date: "[Year]"
physical_description:
  format: "[8vo, 4to, folio, etc.]"
  pages: "[Page count]"
digital_source:
  repository: "[HathiTrust / Internet Archive / other]"
  url: "[URL]"
  ocr_reliability: "[high / moderate / low]"
verification_status: V1
---
```

For historical editions, `atlas_id` is generated by Voice Atlas, not imported from WorldCat. Pattern: `[SURNAME]-[YEAR]-[PLACE]` (e.g., `MAFFEI-1562-NAPOLI`, `TOSI-1723-BOLOGNA`).

The `source_type: historical_edition` tag signals to users that this source predates modern bibliographic systems and has been catalogued to DCRM (Descriptive Cataloging of Rare Materials) standards. This is a category, not a deficit.

---

## 9. The entry template

Every Voice Atlas concept entry contains the following fields.

**Universal fields (all entry types):**
- Entry type, primary language, origin, canonical term, search aliases
- Contributor name and credentials, conflict of interest declaration
- Core claims — each with: Claim, Source (page-level), Claim type, Status, Kernel
- Claim status summary table
- Temporal evolution
- Lineage connections
- Conceptual tags
- See also
- Source records

**Claim types taxonomy:**
- Direct Observation
- Prescriptive Technique
- Empirical Finding
- Transmitted Tradition
- Speculative Extension
- Interpretive Synthesis
- Useful Metaphor (Ian Howell's "useful lie" category)
- Disproven / Historical

**The Kernel:** A mandatory one-line blunt assertion in the founding author's voice, appearing after the Status field in every claim block. No hedging. Plain language. The only field where the founding author's editorial voice is explicitly present.

**Claim status options:** Accepted, Accepted with scholarly caution, Widely cited, Influential but contested, Contested, Useful metaphor / physiologically imprecise, Disproven, Open

---

## 10. The verification gradient

Every claim carries a verification status. No claim reaches `03-Atlas-Staging` without at least V1.

| Status | Meaning |
|---|---|
| **V0** | AI extraction pending human verification |
| **V1** | Founding author verified against physical copy or page image |
| **V2** | Trusted curator verified from their own copy |

**The Verification Dashboard** lives at `04-Verification-Queue/!Verification-Queue.md`:

```markdown
| Source | Claim | Page | Status | Verifier | Date |
|--------|-------|------|--------|----------|------|
| Stark Ch4 | Appoggio requires... | 92 | V1 | DAM | 2026-03-20 |
```

**Rule:** Never move AI-extracted text to `03-Atlas-Staging` without V1 verification.

For historical editions, V1 means verified against the digitized page image (HathiTrust or Internet Archive), not just the OCR text. OCR errors in historical typefaces are common.

---

## 11. The ingestion pipeline

### Scale

389 volumes × average 8 significant claims per volume = approximately 3,100 verified claims total. Estimated extraction work: 600-800 hours. This is years of work. The pipeline must be sustainable for one person teaching full time.

**Pacing recommendation:** Sessions beyond 45 minutes show declining accuracy. Dann determines session length based on cognitive load. Marathon sessions are not recommended, particularly given AuDHD hyperfocus can mask fatigue.

### Setup (completed March 21, 2026)

1. Obsidian vault `VoiceAtlas-Seed` created at `/Users/dannmitton/Documents/VoiceAtlas-Seed`
2. Six-folder structure created inside vault
3. Zotero 8.0.4 confirmed installed
4. Better BibTeX plugin installed and enabled in Zotero
5. Zotero Integration plugin (v3.2.1, mgmeyers) installed and enabled in Obsidian; Note Import Location set to `02-Reading-Notes`
6. Zotero Connector installed in Chrome browser
7. GitHub repository created at `github.com/DannMitton/VoiceAtlas-Seed`; GitHub Desktop connected; initial push completed
8. ABBYY FineReader — install when first pre-1800 source is processed

**Fallback if Zotero-Obsidian plugin breaks:** Export citation from Zotero manually, paste into Obsidian. Do not stop work to fix plugins.

### Bibliographic capture (do for every book before reading)

9. For modern books: search WorldCat (worldcat.org) for the exact edition; use Zotero Connector in browser to save directly to Zotero
10. For pre-1800 sources: skip WorldCat; go to HathiTrust or Internet Archive; download PDF if available; create Obsidian note using the Historical Edition YAML template (Section 8); generate `atlas_id` using pattern `[SURNAME]-[YEAR]-[PLACE]`
11. Tag immediately in Zotero: `atlas-primary` (deep extraction) or `atlas-reference` (peripheral works)
12. Pin citekey in Zotero: right-click item → Better BibTeX → Pin BibTeX key

### Reading and extraction (OCR-first)

13. **Modern books (1800-present):** Scan chapter to PDF → open in Preview on macOS → use Live Text (Ventura or later) to select and copy text → paste into Obsidian reading note titled `YYYY-MM-DD-[citekey]-Ch[N]`
14. **Historical books (pre-1800):** ABBYY FineReader → export as searchable PDF → copy text
15. **Manuscripts (handwritten):** Screenshot and manual transcription only — do not attempt OCR
16. **Screenshots:** Use only for figures, tables, or passages where formatting carries meaning; not for running prose
17. Tag each claim in the reading note using the standard format:

```markdown
> [Pasted or transcribed text] (p.XX)

**Claim:** [One-sentence summary]
**Type:** [DirectObservation / Prescriptive / Empirical / etc.]
**Status:** V0
**AtlasNode:** [Concept name, e.g., "Appoggio"]
```
**Reading note YAML tag convention:**

- Always include: `reading-note`, `V0`
- Then add content topic keywords only — no chapter numbers, no author names, no book titles
- Keywords should name the specific concepts discussed in that chapter (e.g., `appoggio`, `vibrato`, `registers`, `legato`)
- The filename already carries the chapter number and citekey; do not duplicate that information in tags
- The `session_log` field must appear as a markdown table in the document body, immediately after the closing `---` of the YAML frontmatter, not inside the YAML itself
### Verification and staging

18. Add all V0 claims to `04-Verification-Queue/!Verification-Queue.md`
19. Verify each claim against the physical copy or digitized page image; update status to V1
20. When a concept entry reaches V1 throughout, move the markdown file to `03-Atlas-Staging`
21. Never move AI-extracted text to staging without V1 verification

### Backups

22. Weekly: export Zotero library (File → Export Library → Better BibTeX JSON); store in `00-Project/backups/`
23. Weekly or after major sessions: push to GitHub via GitHub Desktop
24. Monthly: review `!Verification-Queue.md`; if V0 items exceed 20, pause new intake and clear backlog

**Note on Dataview plugin (deferred):** Kimi suggested a weekly JSON export via Obsidian's Dataview plugin. This is a good practice but requires plugin configuration that is not appropriate for day one. Defer until Dann is comfortable in Obsidian. Use manual file copy or Zotero export as interim backup.

### PDF collection (pending)

Dann has PDFs not yet catalogued in Libib, including historical Italian texts (some handwritten or manually typeset). These are held in `05-PDFs-Pending` until a dedicated processing session. A specialist workflow for manuscript and early-print materials will be designed at that time.

---

## 12. The tool stack

| Tool | Purpose | Status |
|---|---|---|
| Zotero 8 | Bibliographic control, WorldCat/OCLC anchor, edition management | Installed and configured |
| Obsidian | Knowledge graph, entry drafting, internal architecture | Installed and configured |
| GitHub Desktop | Version control, remote backup | Installed and connected |
| DEVONthink | Reading notes, annotations, clippings | Learn second |
| ABBYY FineReader | OCR for pre-1800 and non-standard typefaces | When first needed |

---

## 13. The GitHub and backup protocol

**Primary working location:** Local Obsidian vault (`VoiceAtlas-Seed`) at `/Users/dannmitton/Documents/VoiceAtlas-Seed`

**Remote backup:** `https://github.com/DannMitton/VoiceAtlas-Seed` (public)

**Backup schedule:** Push to GitHub every Sunday, and after any session producing a new confirmed entry or document

**How to push:** Open GitHub Desktop → confirm changes shown → type summary → Commit to main → Push origin

**Session end:** Claude will specify what changed and what needs syncing.

---

## 14. The collaboration model

**Dann Mitton** — founding author, continuous thread, broker between Claude instances, final editorial authority

**Claude** — project manager, code builder, synthesis engine, drafting support; sculpting role, not authoring role

**Kimi** — architecture, design, UX lead; data model must be resolved before wireframes

**The brokerage model:** Dann pastes this Project File at the start of each new thread. He brings queries from one instance to another. The documents are the institutional memory.

---

## 15. Key relationships and disclosures

- Dann served as editor of Ian Howell's *Hearing Singing* (Rowman & Littlefield, 2025) — declare in any entry engaging that volume
- Ian Howell's *Journal of Singing* article "Stand on the Shoulders of Giants" (Vol. 74, No. 3, Jan/Feb 2018, pp. 325–328) is a founding intellectual reference for Voice Atlas
- The Aspen Grove project (theaspengrove.org, Seth Keeton) maps pedagogical lineage; Voice Atlas interoperates with it, not duplicates it

---

## 16. Publisher peer review taxonomy

*Public-facing on source records; legend available on demand.*

| Tier | Label |
|---|---|
| Double-blind peer reviewed | OUP, CUP, University of Toronto Press, Rowman & Littlefield, Pendragon Press |
| Single-blind peer reviewed | Selected academic publishers |
| Editor-reviewed | Inside View Press (Scott McCoy), SMT Press (Cheri Montgomery) |
| Self-published | No external review process |
| Unknown | Review process not documented |

Publisher tier informs scrutiny; it does not determine inclusion.

---

## 17. Dissertation policy

Evaluated on the same citation-first standard as every other source. Follow citations to primary literature before publishing any claim drawn from a dissertation. The dissertation is the map, not the treasure.

---

## 18. Open question for Kimi

The YAML format Kimi specified in her handoff brief uses `atlas_id: STARK-2003-BELCANTO-CH4` — this appears to key an entry to a source chapter rather than a concept node. Voice Atlas entries are keyed to concepts (people, terms, lineages), not to source chapters. Reading notes are keyed to source chapters.

**The question:** Does Kimi's target format describe a reading note or a concept entry? If a concept entry, the YAML structure needs adjustment to reflect that one concept entry aggregates claims from multiple sources. If a reading note, the handoff format for the static site still needs to be specified separately.

Awaiting Kimi's clarification before finalising the file format standard.

---

## 19. Pending deliverables

**Short term:**
- Miller case study — *National Schools of Singing* (1977) vs. later Miller works
- Node Authority Research — Grove's, *Journal of Singing* index
- Aspen Grove integration analysis
- Finalise concept entry file format once Kimi clarifies the reading note vs. concept entry question

**Ongoing:**
- Attentive reading of twelve primary corpus books
- 3,100 verified claims total across 389 volumes
- 60-entry seed threshold for seeded release

---

## 20. Current state

*Updated at the end of every working session.*

**Last updated:** March 21, 2026 — Session 2

**Completed this session:**
- VoiceAtlas-Seed Obsidian vault created at `/Users/dannmitton/Documents/VoiceAtlas-Seed`
- Six-folder structure created: `00-Project`, `01-Entries`, `02-Reading-Notes`, `03-Atlas-Staging`, `04-Verification-Queue`, `05-PDFs-Pending`
- Zotero 8.0.4 confirmed installed
- Better BibTeX plugin installed and enabled in Zotero
- Zotero Integration plugin (v3.2.1, mgmeyers) installed and enabled in Obsidian; Note Import Location set to `02-Reading-Notes`
- Zotero Connector installed in Chrome browser
- Stark, *Bel Canto* imported to Zotero from WorldCat; citekey `starkBelCantoHistory1999` pinned; tagged `atlas-primary`
- `!Verification-Queue.md` created in `04-Verification-Queue` with table structure
- GitHub repository created: `github.com/DannMitton/VoiceAtlas-Seed` (public)
- GitHub Desktop installed and connected to local vault
- All founding documents copied into `00-Project`; `entry_appoggio.md` copied into `03-Atlas-Staging`
- Initial commit pushed to GitHub: "Initial commit — founding documents and appoggio entry"

**Files in vault as of this session:**
- `00-Project`: PROJECT_FILE versions 1.1–1.5, STYLE_SHEET.md, FOUNDING_DOCUMENT.docx, all Kimi briefs and responses
- `03-Atlas-Staging`: entry_appoggio.md
- `04-Verification-Queue`: !Verification-Queue.md

**Next session begins with:**
Step 1: Open Stark's *Bel Canto*, Chapter 4. Begin attentive reading and extraction into a new reading note in `02-Reading-Notes`, following the ingestion pipeline (Section 11).

---

## 21. Term origin taxonomy (confirmed March 20, 2026)

Every concept entry carries a `term_origin` classification. This determines the display header and attribution mode.

| Value | Meaning | Display title | Example |
|---|---|---|---|
| `traditional` | Term predates any single author; part of centuries-old conversation | **Term** only | **Appoggio** |
| `coined` | Author invented the terminology or framework | **Term (Author)** | **Primal Sounds (Chapman)** |
| `uncertain` | Origin unclear — flag for verification pass, keep reading | **Term** pending resolution | |

**The 19th-century litmus test:** Could this term have appeared in a pre-20th-century treatise? If yes, it is traditional. If no, it is probably coined. Apply this test during reading sessions. If genuinely uncertain, mark `term_origin: uncertain` and move on — do not stop the reading session to research it.

**For Italian, French, or German terms:** Assume traditional unless proven otherwise.

**Additional YAML fields for concept entries:**
```yaml
term_origin: traditional         # traditional / coined / uncertain
attribution_mode: provisional-consensus  # proprietary / provisional-consensus / consensus
first_attestation: "Lamperti school, late 19th c."  # For traditional terms
coined_by: chapman2011singing    # For coined terms only
```

**Attribution modes:**
- `proprietary` — coined term, single source is correct and complete
- `provisional-consensus` — traditional term, single source so far
- `consensus` — traditional term, two or more sources

---

## 22. Confirmed decisions from Augure consultation (March 21, 2026)

**Adopted from Augure:**
- Stanford Encyclopedia of Philosophy and Perseus Digital Library added to the interface survey list alongside Connected Papers, Kumu, Obsidian graph view, and The Pudding
- ATLAS.ti and MAXQDA noted as qualitative research tool analogues — useful for thinking about claim taxonomy
- Progressive disclosure tiers (discovery / exploration / contribution) confirmed as a Phase Two UX concept for Kimi; not a YAML content field

**Rejected from Augure:**
- `scope: western-classical` in YAML — directly contradicts the founding document scope statement; Voice Atlas scope is explicitly inclusive of all singing traditions
- Dataview plugin as short-term priority — already explicitly deferred; zero-config principle stands
- `filters` field in YAML — conflates content metadata with UI state; filters are Kimi's interface layer decision

**Deferred from Augure (Phase Two or later):**
- Knowledge graph JSON export and D3.js / Cytoscape.js — Phase Two, Kimi's territory
- Elasticsearch — overkill for 3,100 claims; Kimi recommends Lunr.js, Fuse.js, or Pagefind; reserve Elasticsearch only if expanding to full-text source search across all 389 volumes
- Guided tour script — cannot write for an interface that does not exist
- GitHub-style claim diffs — Phase Three contribution pipeline

---

## 23. Confirmed: `tier` field removed from YAML standard

Progressive disclosure tier is derived state, not content metadata. Kimi derives it at build time from existing fields (`claim_type`, `verification_status`, `concept_nodes`). No manual field required during ingestion. Removed from YAML standard entirely.

---

## 24. Confirmed: `lineage` array replaces scope field

Instead of any scope field, concept entries carry an optional `lineage` array describing inheritance without predefining boundaries:

```yaml
lineage:
  - bel-canto
  - italian-school
```

or

```yaml
lineage:
  - estill
  - afro-american-gospel
```

This supports the mapping purpose without exclusionary defaults.

---

## 25. Confirmed: Full concept entry YAML standard

This is the confirmed format for all concept entries in `03-Atlas-Staging`:

```yaml
---
concept_id: [canonical-node-name]
node_type: concept  # concept / person / source / lineage / technique
display_name: "[Display name]"
term_origin: traditional  # traditional / coined / uncertain
attribution_mode: provisional-consensus  # proprietary / provisional-consensus / consensus
first_attestation: "[Earliest known usage]"  # for traditional terms
coined_by: [citekey]  # for coined terms only
lineage:
  - [lineage-tag]
aliases:
  - "[Search alias 1]"
  - "[Search alias 2]"
date_created: YYYY-MM-DD
last_modified: YYYY-MM-DD
entry_status: staging  # draft / staging / published
sources:
  - citekey: [citekey]
    pages: "[Page range]"
    claims: ["claim-001", "claim-002"]
claim_count: [N]
verifier: "Mitton, Daniel A."
verification_status: V1
---
```

The *appoggio* prototype entry needs to be reformatted to this standard before moving to `03-Atlas-Staging`.

---

## 26. Confirmed: `session_log` field added to reading note YAML

Kimi's suggestion — accepted immediately. AuDHD hyperfocus can mask depletion. A lightweight session log gives Dann data for self-regulation without requiring active monitoring during sessions.

Add to every reading note YAML:

```yaml
session_log:
  - date: YYYY-MM-DD
    duration_mins: [N]
    cognitive_state: fresh  # fresh / moderate / fatigued
    interruptions: [N]
    notes: "[Optional brief note]"
```

Thirty seconds at session end. Worth it.

---

## 27. Interface survey list (current)

When Dann has three to five concept entries in `03-Atlas-Staging`, survey these before briefing Kimi for Phase Two:

- Connected Papers (connectedpapers.com)
- Kumu (kumu.io)
- Obsidian graph view (already installed)
- The Pudding (pudding.cool)
- Stanford Encyclopedia of Philosophy (plato.stanford.edu)
- Perseus Digital Library (perseus.tufts.edu)
- Old Weather (oldweather.org) — for contribution form mechanics

Note what feels right and what frustrates. That feedback is the brief.
