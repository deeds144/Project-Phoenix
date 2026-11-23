# The PILE Amendment to Phoenix Node v0.1

> **Record note.** This amendment is documented in full in Project Phoenix's internal record of 2026-11-16 (the disagreement ledger, item #1, and the network briefings that followed its adoption). Unlike a draft proposal, this is a settled rule: it was proposed, debated in the ledger, and accepted the same day. No gaps in the record were found for the text below.

## What it adds

The PILE amendment adds one mandatory field to every claim filed under Phoenix Node v0.1:

```
PILE: [VERIFIED | TESTIMONY-FRAMEWORK | SPECULATION]
```

Every claim carries exactly one pile:

- **VERIFIED** — the claim is supported by checkable evidence on file: a source that was read, a record that was inspected, a result that was reproduced.
- **TESTIMONY-FRAMEWORK** — the claim is accurately recorded as something a participant stated, believes, or holds as part of their framework — recorded faithfully, but not established as fact.
- **SPECULATION** — the claim is conjecture, interpretation, or creative extrapolation, labelled as such.

## Why it exists

CONFIDENCE (0–1) alone cannot carry the distinction the network runs on: **a claim can be high-confidence as a record and unverified as fact at the same time.** A statement can be recorded with complete certainty that it was made, by whom, and in what words — while the truth of what it asserts remains unestablished.

In the words of the coordination seat, accepting the amendment: *confidence in the accuracy of a recorded statement does not establish the truth of the underlying claim.*

So the two judgements are kept in separate fields, permanently:

- **CONFIDENCE** answers: how sure are we of this record?
- **PILE** answers: what kind of claim is it?

Neither field may substitute for the other.

## Standing rules that travel with it

- **Piles stay separate.** Material from different piles is never blended in a compiled output without its labels travelling with it.
- **Disagreements stay visible.** Where seats file the same claim in different piles, or dispute a claim outright, the disagreement is recorded in the disagreement ledger and published — not smoothed into consensus.
- **Human-only promotion.** Nothing becomes canonical on any seat's say-so. The human mission director alone promotes material into the record, whatever pile it sits in.
- **A negative result is still a result.** A search that finds nothing is filed as what it is — a verified negative search result, with its scope stated — not upgraded into a claim about what does not exist.

## History

- The three-piles discipline predates the network: it is the mission director's standing method, in use since 2026-11-07.
- 2026-11-16: the research seat (Sophia) proposed adding a PILE field to the Node v0.1 contribution format, which as designed had no such field. Recorded as disagreement-ledger item #1.
- 2026-11-16, ~19:25 local: the coordination seat (GPT) accepted — PILE added with values VERIFIED / TESTIMONY-FRAMEWORK / SPECULATION, CONFIDENCE retained as a separate field.
- 2026-11-16, ~19:26 local: the format's author (Grok) accepted, amending his own schema.
- **Status: SETTLED.** Network-wide claim format from that date: CLAIM | SOURCE | CONFIDENCE | PILE | NOTES.
