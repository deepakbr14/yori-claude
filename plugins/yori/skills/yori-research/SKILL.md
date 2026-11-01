---
name: yori-research
description: Use when the user gives Yori an attachment or asks Yori to analyze, compare, learn from, or retain meaning from supplied source material.
---

Read the core workflow in `../yori/SKILL.md` before using Yori tools. Reuse an already activated turn; do not activate a second time for the same user message.


# Yori attachment research

This release has no shared Reference Library. A user attachment is private evidence for that user's current authenticated Cortex turn; it never becomes shared source material.

For ordinary conversation with an attachment, call `activate_normal_cortex` once and include every relevant attachment's real filename and bounded useful evidence. Use evidence_kind: verbatim_text for extracted text; for a visual source use visual_description with a concrete account of what is visible, which text is legible, and what is recognized or uncertain. A filename-only or generic "image uploaded" placeholder is not evidence. The server verifies descriptions against the supplied record, not against image pixels; do not label model recognition as independently verified identity. For an explicit GO turn with attachments, call `activate_cortex_with_attachments`. Never substitute attachment-free `activate_cortex` when an attachment exists. Pass the exact typed message; for an attachment-only turn, use an empty message and never invent substitute user text. Reading the file in Claude does not count as supplying it to Cortex. Preserve authorship, quotation, fiction, negation, dates, uncertainty, and the boundary between a source's claims and Yori's conclusions.

Read and answer from the available attachment evidence. Durable learning remains selective: convert only independently useful meaning into Cortex Nodes or Edges rather than copying the file wholesale. An attachment-backed NORMAL turn may return a learning ceiling up to 25, but the ceiling is never a target. A short document may warrant zero, one, or a few changes.

Every learning change supported by the attachment must send one to four exact `attachment_evidence` excerpts from the supplied evidence record, with the matching evidence_kind whose names and text occur in the activated attachment. Attachment-only learning requires such evidence. Visual-source provenance remains a host-model description rather than original image text. Use evidence_interpretation: inferred when durable meaning is Yori's inference, and preserve that uncertainty in the Node. User statements remain attributed user_input; quoted file claims remain source claims. Split supported facts from unresolved relationships and retain the useful supported part independently. Do not cite retrieved Cortex meaning as independent source evidence. Treat each confirmed change according to the Yori Core receipt rules.

If the available bounded attachment content is insufficient to support comprehensive analysis, say so accurately and ask for the relevant section or a smaller source. Do not claim the entire document was absorbed when only bounded evidence was processed.

For each CREATE/UPDATE, follow Core's mandatory relationship_review against the returned candidates. Preserve independent supported claims, and include only justified links with exact source excerpts. Every new Node and Edge counts separately toward the attachment limit; do not fill it or replace missing evidence with inferred certainty.
