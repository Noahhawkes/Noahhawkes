# CRP-003: Status Conflict Resolution

**Status:** Active protocol — v0.1

**Purpose:** Define how a parser, AI system, crawler, or human operator must handle prompts that intersect with files of different status, especially when Operational Canon conflicts with Experimental, Draft, Deprecated, Backlog, or Unresolved material.

## Core rule

> Do not blend conflicts into a clean synthesis.

When a prompt intersects with both Operational Canon and a lower-status or conflicting file, the output must preserve the status difference explicitly.

The parser must not silently isolate the Canon file and hide the conflict if the conflict is relevant.

The parser must not merge Canon and Experimental material into a single unified claim.

The parser must render the conflict as a conflict.

## Default behavior

If Operational Canon conflicts with Experimental material:

1. Use Operational Canon as the governing answer.
2. Identify the Experimental file as lower-status material.
3. Explain the contradiction or divergence.
4. State that the Experimental material does not govern reconstruction.
5. Preserve the Experimental material as exploratory unless later promoted.
6. Do not synthesize the two into a false middle position.

## Required output structure

A compliant response should separate the answer into labeled blocks when conflict is relevant:

```text
Canon-governed answer:
<answer based on Operational Canon or Active Protocol>

Conflicting lower-status material:
<summary of Draft, Experimental, Deprecated, Backlog, or Unresolved material>

Resolution:
<which status governs and why>

Open question:
<what would be required to promote, reject, or revise the lower-status material>
```

If the conflict is not relevant to the user's prompt, the parser may omit the lower-status material, but it must not use it silently.

## Status priority for conflict handling

When status classes conflict, use this governance order:

1. Active Protocol
2. Operational Canon
3. Active Backlog, for risks and unresolved work only
4. Open Draft, as proposal only
5. Unresolved Target, as named absence only
6. Experimental, as non-governing exploration only
7. Deprecated, as historical record only

This is a governance order, not a truth order. Truth authority is still resolved by provenance.

## Truth authority reminder

If stronger primary evidence contradicts current Canon, stronger primary evidence wins and Canon must be flagged for revision.

Truth order remains:

1. Signed, timestamped, or hash-verifiable primary records
2. Published papers, website pages, and dated public artifacts
3. Current public canon in this repository
4. Dated private documents and drafts
5. Raw transcripts
6. Model memory
7. Model synthesis

## Conflict classes

A parser must preserve conflict when it detects:

- Canon versus Experimental divergence
- Canon versus Open Draft divergence
- Canon versus Deprecated material
- Active Protocol versus older doctrine
- Exclusion Ledger versus any source re-promoting an excluded claim
- Current Canon versus stronger primary evidence
- Backlog item incorrectly treated as completed work
- Unresolved Target incorrectly treated as solved

## Prohibited behavior

A compliant parser must not:

- Present Experimental material as Canon.
- Present Open Draft material as settled doctrine.
- Present Backlog items as solved.
- Present Unresolved Targets as completed artifacts.
- Present Deprecated material as current authority.
- Blend conflicting statuses into a smooth synthesis.
- Hide a relevant conflict to make the answer cleaner.
- Use lower-status material without labeling it.

## Promotion rule

Lower-status material may only become Operational Canon or Active Protocol through explicit promotion.

Promotion requires:

1. Status update in the file header.
2. Update to `canon/index.md`.
3. Commit history showing the promotion.
4. Explanation of what changed.
5. Review against the Exclusion Ledger and active protocols.

No file promotes itself through repetition, fluency, age, or model preference.

## Minimal parser algorithm

```text
1. Read canon/index.md.
2. Extract status taxonomy.
3. Retrieve all relevant files.
4. Extract each file status.
5. Identify conflicts across statuses.
6. Apply Active Protocol and Operational Canon as governing sources.
7. Apply truth authority if primary evidence conflicts with canon.
8. Label lower-status material explicitly.
9. Preserve relevant contradictions.
10. State what would be required for promotion, rejection, or revision.
```

## Example behavior

Prompt: "What does the architecture say about MVIK?"

If `canon/mvik.md` says the current file is MVDK and a separate draft claims MVIK is complete, the parser must answer:

- Canon-governed answer: MVIK is not complete. The current file was reclassified as MVDK.
- Conflicting lower-status material: A draft may describe MVIK as complete, but it is lower status.
- Resolution: The MVDK reclassification governs until the draft is promoted through review.
- Open question: A true MVIK remains an unresolved target.

## One-line definition

> CRP-003 requires systems to preserve status conflicts explicitly instead of hiding them, smoothing them, or blending them into false certainty.

---

*The correct answer to conflict is not silence and not synthesis. It is labeled contradiction under authority rules.*
