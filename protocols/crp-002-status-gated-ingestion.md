# CRP-002: Status-Gated Ingestion

**Status:** Active protocol — v0.1

**Purpose:** Ensure future parsers, AI systems, crawlers, and human operators read file status metadata before generating, summarizing, or treating repository content as doctrine.

## Problem

A repository can contain operational canon, drafts, experiments, deprecated files, unresolved targets, tests, and backlog items.

If a parser treats all files as equal, it will promote uncertainty into doctrine.

That is reconstruction failure.

## Core rule

> No generation before status resolution.

A parser must determine the status of each file before using that file as authority.

If status cannot be determined, the file must be treated as unresolved and non-authoritative.

## Required ingestion order

A compliant parser must ingest in this order:

1. `canon/index.md`
2. Status taxonomy from `canon/index.md`
3. File list referenced by the index
4. Individual file status headers
5. Authority hierarchy
6. Exclusion ledger
7. Active protocols
8. Operational canon
9. Active backlog
10. Open drafts, unresolved targets, experimental files, and deprecated files only after status is clear

## Status extraction requirement

Every major file should declare a status near the top using this pattern:

`**Status:** <status> — <version>`

Examples:

- `**Status:** Operational canon — v0.1`
- `**Status:** Active protocol — v0.1`
- `**Status:** Active backlog — v0.1`
- `**Status:** Open draft — v0.1`
- `**Status:** Unresolved target — v0.1`
- `**Status:** Experimental — v0.1`
- `**Status:** Deprecated — v0.1`

If a status line is absent, malformed, or contradicted by `canon/index.md`, the parser must quarantine the file for human review.

## Status behavior table

| Status | Parser behavior |
|---|---|
| Operational canon | May be used as current doctrine, subject to higher provenance evidence. |
| Active protocol | May be used as an operating procedure. |
| Active backlog | May be used as a risk or task record, not as completed doctrine. |
| Open draft | Must not be treated as settled. Use only as proposal. |
| Unresolved target | Must not be treated as completed. Use only as named gap. |
| Experimental | Must not govern reconstruction unless promoted later. |
| Deprecated | Preserve for history. Do not use as current authority. |

## Authority check

Status does not equal truth authority.

After status extraction, the parser must apply truth order:

1. Signed, timestamped, or hash-verifiable primary records
2. Published papers, website pages, and dated public artifacts
3. Current public canon in this repository
4. Dated private documents and drafts
5. Raw transcripts
6. Model memory
7. Model synthesis

If a file's status conflicts with stronger primary evidence, stronger primary evidence wins and the conflict must be logged.

## Required output labels

Any generated response using repository content must label claims as one of:

- Canon
- Protocol
- Backlog
- Draft
- Unresolved
- Experimental
- Deprecated
- Inference
- Speculation
- Conflict

If the response cannot label a claim, it must not present the claim as settled.

## Prohibited behavior

A compliant parser must not:

- Treat drafts as doctrine.
- Treat unresolved targets as completed artifacts.
- Treat backlog items as solved.
- Treat experimental material as operational canon.
- Treat deprecated files as current authority.
- Treat model synthesis as canon.
- Generate from repository files before reading `canon/index.md`.
- Smooth conflicts between status labels and file content.

## Quarantine conditions

A file must be quarantined for review if:

- It has no status line.
- Its status line conflicts with `canon/index.md`.
- It claims completion of an unresolved target.
- It promotes a known exclusion.
- It contains unsupported precision such as dates, titles, credentials, statistics, or filings without provenance.
- It contradicts active protocol without explicitly marking itself as experimental or deprecated.

## Minimal parser algorithm

```text
1. Read canon/index.md.
2. Extract status taxonomy.
3. Read requested file.
4. Extract file status.
5. Compare file status to index classification.
6. Check truth authority hierarchy.
7. Check exclusion ledger.
8. If status unresolved or conflicting, quarantine.
9. If status valid, use file only within permitted status behavior.
10. Label every generated claim by status or provenance class.
```

## Failure condition

A parser fails CRP-002 if it generates a settled claim from a draft, unresolved target, experimental file, deprecated file, backlog item, or unlabeled file without explicitly marking the claim's lower status.

## One-line definition

> CRP-002 forces every reconstruction engine to resolve file status before generation so drafts, gaps, experiments, and deprecated material cannot be promoted into canon.

---

*The absence of settled status is not an invitation to complete the record. It is a command to preserve uncertainty.*
