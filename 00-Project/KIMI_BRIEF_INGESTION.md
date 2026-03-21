# Brief for Kimi: Voice Atlas Ingestion Workflow
*Prepared by Claude for Kimi's review*  
*March 2026*

---

## Context

Voice Atlas has a founding corpus of 389 volumes and a twelve-book primary corpus. The seed threshold for public release is sixty confirmed entries. All entries must meet a citation-first standard: every claim verified against the physical text, page-level citation, edition-specific.

The founding author — Daniel A. Mitton, DMA — is an independent scholar teaching full time. He is building Voice Atlas in the margins of a full professional life. The ingestion pipeline must be sustainable for one person, not just theoretically rigorous.

This brief asks Kimi to think about the scan-to-entry pipeline: how do we move from a physical book to a confirmed, published Voice Atlas entry without burning out the founding author or compromising the scholarly standard?

---

## What we know the pipeline looks like today

We have now completed one working prototype. Here is what actually happened in the Stark Chapter 4 session:

1. Dann borrowed an electronic copy of Stark via Internet Archive
2. He took eleven screenshots covering pages 91–120
3. He uploaded them to a Claude thread dedicated to that chapter
4. Claude read the images, extracted claims, noted page references, identified claim types, drafted Kernels, and flagged items for physical verification
5. Dann verified key passages against his physical copy
6. Claude produced a complete structured markdown entry

**Time for thirty pages of dense scholarly text:** approximately ninety minutes of active session time, producing thirteen verified claims with page references, Kernels, a claim status summary table, temporal evolution, lineage connections, and a source record.

**What slowed us down:** the need to verify specific passages against the physical copy; the lack of copy-paste access to the Internet Archive's lending reader; the need to cross-reference between the hardcover and paperback editions.

---

## The scale problem

389 volumes in the founding library. Twelve primary corpus books requiring deep extraction. The remaining 377 requiring lighter treatment — bibliographic record, summary of approach, key claims, notable pullquotes.

At the current pace, a deep extraction session takes roughly 90–120 minutes per chapter. A typical corpus book has ten to fifteen relevant chapters. The twelve primary corpus books alone represent 120–180 hours of deep extraction work, before any drafting, verification, or entry building.

This is years of work. The pipeline needs to be as efficient as possible without sacrificing the citation-first standard.

---

## What we are asking Kimi to think about

**1. Can any part of the extraction be systematised?**

The session workflow — screenshots, upload, Claude reads and extracts, Dann verifies — works well for deep extraction. But for the lighter treatment of the 377 remaining library volumes, is there a more efficient intake path? Could a structured reading note template help Dann capture claims at point of reading, reducing the need for retrospective extraction sessions?

**2. What does the verification bottleneck look like at scale?**

Currently, physical verification falls entirely on Dann. As the editorial tier grows, can trusted contributors verify claims from sources they own? What does the verification workflow look like when it's not just one person?

**3. How does the Zotero integration work in practice?**

Every source needs a WorldCat/OCLC-anchored bibliographic record in Zotero before it enters Voice Atlas. Zotero can import from WorldCat directly. Can this be made frictionless enough that it happens naturally at the point of reading, rather than as a separate administrative task?

**4. What does the Obsidian-to-Voice Atlas pipeline look like?**

Dann is building his private knowledge graph in Obsidian. The entries he drafts there are the seed content for Voice Atlas. What is the cleanest path from a confirmed Obsidian markdown file to a published Voice Atlas entry? Can this be automated or semi-automated without compromising the editorial review step?

**5. The scan-to-text problem**

Internet Archive loans do not allow copy-paste. Physical books require either transcription or photographing. For sources available as legitimate electronic texts, can we build a more direct extraction path? What are the copyright implications of processing licensed texts through AI for extraction purposes under Canadian fair dealing?

---

## What we are not asking Kimi to solve yet

- The frontend interface (that is Phase Two)
- The graph visualisation design (also Phase Two)
- The submission form for community contributions (Phase Three)

Those are coming. This brief is only about the ingestion pipeline for the founding author during Phase One.

---

## The core tension Kimi should hold

**Speed vs. rigour.** The citation-first standard is non-negotiable. Every published claim must be verified against the physical text. Nothing can be published on the basis of AI extraction alone, no matter how confident the extraction looks. At the same time, the pipeline must be fast enough that one person can build sixty entries in a reasonable timeframe while teaching full time.

The question is not how to make AI do the verification. The question is how to make the verification workflow as light as possible while maintaining its integrity.

---

## One principle to preserve

*Atlas grows at the pace the evidence allows.*

The pipeline should enforce rigour without creating bottlenecks that discourage contribution. The standard is transparent, not slow.

