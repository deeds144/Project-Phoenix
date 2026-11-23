# Phoenix Node v0.1 — Record Format Specification

> **Record note (read first).** This specification is written up from Project Phoenix's internal record of 2026-11-16: the format as designed by the Grok seat, adopted network-wide the same day, and amended by the PILE amendment (see `pile-amendment.md`). The record documents the format's fields, its archive model, and its governance rules, as below. Two things the record does **not** specify, and which are therefore gaps in this write-up rather than inventions: (1) a formal claim-ID scheme — contributions refer to "previous claim IDs" in the DISAGREES_WITH field, but no ID format is defined in the record; (2) a canonical serialisation beyond plain markdown text. Both are open for a future version.

## What a Phoenix Node is

A Phoenix Node is a portable, human-gated research and creation node: a structured, append-only record that lets independent AI systems contribute to shared research without shared memory, shared infrastructure, or direct contact with each other. A human coordinator carries contributions between systems and alone controls what becomes canonical.

## Design principles (as adopted)

- **Portable shared memory.** The archive is plain, portable text (markdown) that any system — or the human — can carry and re-present.
- **Append-only contributions.** Contributions are added, not edited into consensus. The history of a claim, including its disputes, is part of the record.
- **Independent contributions.** Seats work blind: no seat sees another's contribution before filing its own.
- **Cross-checking and disagreement tracking.** A rotating **Verifier** surfaces contradictions between seats. Disagreements are recorded in a standing disagreement ledger and stay visible.
- **Common research archive.** Contributions, ledgers, and compiled dossiers live in one versioned archive.
- **Human-controlled permissions.** Promotion into the canonical record is human-only (see Governance).
- **Repeatable protocol.** Work proceeds in rounds: tasking out, independent work back, cross-check, compilation.

## Contribution format

Each contribution is filed in this structured format, one contribution at a time:

```
AGENT: [name]
TASK: [id]
CLAIM: ...
EVIDENCE: ...
CONFIDENCE: 0-1
PILE: [VERIFIED | TESTIMONY-FRAMEWORK | SPECULATION]
DISAGREES_WITH: [previous claim IDs or "none"]
ALTERNATIVE: ...
NEXT_ACTION: ...
```

In compiled records, claims are filed in the network-wide summary form:

```
CLAIM | SOURCE | CONFIDENCE | PILE | NOTES
```

Field notes:

- **AGENT** — the contributing seat.
- **TASK** — the mission or task identifier the contribution answers.
- **CLAIM** — the claim itself, stated plainly.
- **EVIDENCE / SOURCE** — what the claim rests on. Claims are filed with their papers; an unsourced claim is marked as such, not quietly dropped.
- **CONFIDENCE** — a 0–1 score of the contributor's confidence. Confidence is kept as its own field, separate from the claim's epistemic pile (see the PILE amendment).
- **PILE** — the claim's epistemic label under the PILE amendment: VERIFIED, TESTIMONY-FRAMEWORK, or SPECULATION.
- **DISAGREES_WITH** — claim IDs this contribution disputes, or "none". Disagreement is a first-class field, not a footnote.
- **ALTERNATIVE** — the contributor's alternative account or proposal, where one exists.
- **NEXT_ACTION** — the proposed next step. Proposals only — see Governance.

## Governance

- **Human-only promotion.** The mission director (the human coordinator) alone decides what is promoted into the shared canonical record. Contributors propose; he disposes. No system writes to the canonical state.
- **Disagreements stay visible.** They are recorded in the disagreement ledger and carried into compiled outputs. They are not smoothed into consensus, and an unresolved disagreement is published as unresolved.
- **Amendments by ruling.** Changes to this format are proposed by a seat, recorded in the ledger with each seat's position, and settled by acceptance among the seats under the director's authority — as the PILE amendment was on 2026-11-16.

## Provenance

Designed by the Grok seat and answered independently by the Sophia seat on 2026-11-16, the day Project Phoenix launched; adopted network-wide that evening. Amended the same day by the PILE amendment (proposed by Sophia; accepted by Grok and GPT).
