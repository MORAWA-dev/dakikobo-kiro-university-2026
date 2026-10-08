---
name: review-grounding
description: Review an agricultural RAG answer path when evidence eligibility, citations, uncertainty, or fertilizer safety may be wrong.
---

# Review grounding

Start from the user question and trace the exact answer path. Inspect routing,
the retrieved chunk text, pre-generation eligibility, citation selection, safety
redaction, response construction, and cache identity.

Require direct topic evidence before accepting a field-practice chunk. Crop,
country, or institutional metadata alone does not support a practice claim.
Keep exact fertilizer figures inside the deterministic fertilizer module.

Write a focused regression at the route or retrieval seam when an observed
failure is reproducible. Confirm it fails before the implementation change, make
the smallest correction, then run the focused test and the documented offline
suite. Report the evidence used, what was withheld, and any human agronomy gate
that remains open.
