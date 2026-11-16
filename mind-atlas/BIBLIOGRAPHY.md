# Annotated Research Bibliography
**Hawkes Mind Atlas | Candidate Public Edition | 16 November 2026**

This bibliography is an **initial verified-link index**, not yet the complete bibliography of every article on the GitHub account. Each primary entry below was opened through the connected GitHub repository interface in the working session. "Inspected" means a document was retrieved and read, **not** that its scientific claims were independently validated, its code executed, or its authorship adjudicated.

The owner has asserted authorship of the articles published on the account. Authorship should be recorded at document level using the author's declaration, file bylines, contribution history, and any later corrections. Where metadata appears inconsistent, the discrepancy belongs in the record, not in a premature verdict. Third-party named references and repository mirrors should be indexed separately from original articles.

## Primary bibliography: directly inspected public sources

### B01. Artificial Continuity: Working Manifesto
**Source:** [`artificial-continuity/docs/ARTIFICIAL_CONTINUITY_MANIFESTO.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/ARTIFICIAL_CONTINUITY_MANIFESTO.md)  
**Type:** Research manifesto / thesis. **Status:** Inspected source; claims proposed.  
**Themes:** intention, memory, state lineage, epistemic integrity, portability, governance, interruption recovery.

**Annotation.** The manifesto identifies a gap between storing information and preserving the evolving trajectory of a human goal. It argues that intentions should be primary objects, that state should retain its provenance, that uncertainty is representable data, and that postponed work must keep its reactivation conditions. It separates model reasoning from authority, and treats divergence as history rather than an error to overwrite. Its most important contribution to the atlas is its coherent articulation of the problem that other documents try to operationalize.

**Critical question:** Which measurable gains are attributable to an explicit continuity layer rather than to standard retrieval, structured state, task management, or an expanded context window?

### B02. Human Intent Graph Protocol (draft 0.1)
**Source:** [`artificial-continuity/docs/HIGP_DRAFT.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/HIGP_DRAFT.md)  
**Type:** Proposed interoperability protocol / schema. **Status:** Inspected draft.  
**Themes:** graph representation, intentions, decisions, evidence, event history, portable memory.

**Annotation.** HIGP defines typed entities for intentions, artifacts, ideas, decisions, claims, assumptions, commitments, events, and user-defined constitutional constraints. It proposes directional relationships such as `SUPPORTS`, `CONTRADICTS`, `DEPENDS_ON`, `SUPERSEDES`, `EVIDENCE_FOR`, and `WAITING_ON`. A key distinction is between derived current state and an append-only event history. The protocol is a plausible foundation for this atlas because it permits concepts, documentary citations, decisions, and revisions to live in a common graph without pretending they are equivalent.

**Critical question:** Can the vocabulary remain stable and interoperable across unrelated tools, users, and research domains?

### B03. Prospective Memory
**Source:** [`artificial-continuity/docs/PROSPECTIVE_MEMORY.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/PROSPECTIVE_MEMORY.md)  
**Type:** Capability design / implementation description. **Status:** Inspected; specific version assertions not independently tested.  
**Themes:** conditional reminders, autonomy, commitments, timing, permission.

**Annotation.** This document asks how a system should remember an intention whose relevance depends on changing conditions rather than an arbitrary future date. It describes a deterministic `ProspectiveMemory/0.1` approach using thresholds, entity states, relationships, dates, and logical combinations. A triggered condition creates a policy-gated proposal rather than silently performing consequential action. The subtle conceptual advance is the distinction between **recognizing relevance** and **receiving authority to act**.

**Critical question:** How do false-positive and missed-trigger rates change with noisier real-world events, partial context, and changing goals?

### B04. Continuity Trust Model v0.7
**Source:** [`artificial-continuity/docs/TRUST_MODEL.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/TRUST_MODEL.md)  
**Type:** Trust and security architecture. **Status:** Inspected design and reported regressions; not a security audit.  
**Themes:** confidentiality, integrity, authenticity, authority, cryptographic provenance.

**Annotation.** The document separates four often-conflated guarantees: who can read a record, whether a record changed, whether an apparent device identity is authentic, and what the device or model is allowed to do. It documents AES-256-GCM encryption for a vault prototype, SHA-256 event chains, experimental ECDSA device identities, and graduated action classes. It also states important limits: a valid signature does not prove real-world identity, and certain recovery and enrollment concerns remain unresolved. Its restraint about what technical controls actually establish makes it a useful methodological reference.

**Critical question:** Can threat modeling, key recovery, device enrollment, and independent security review substantiate a production deployment?

### B05. Continuity Architecture
**Source:** [`artificial-continuity/docs/ARCHITECTURE.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/ARCHITECTURE.md)  
**Type:** System design. **Status:** Inspected architecture, not full implementation verification.  
**Themes:** event sourcing, state reduction, proposals, constitutional constraints, branching, portability.

**Annotation.** This architecture lays out a chain from capture and structured observation to reasoning, action proposal, policy evaluation, approval, append-only event, reducer, and resumable derived state. It specifies autonomy levels, distinguishes proposals from approved actions, and describes cognitive branches as alternate histories of an intent graph. The design makes a concrete engineering claim: a model can be replaceable if the continuity semantics, events, permissions, and artifacts remain externally inspectable.

**Critical question:** Which modules are currently operational in which tested environment, and how are those boundaries represented without drift?

### B06. Project Constellation
**Source:** [`artificial-continuity/docs/PROJECT_CONSTELLATION.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/PROJECT_CONSTELLATION.md)  
**Type:** Operational state / release-evidence design. **Status:** Inspected; reported tests not independently reproduced.  
**Themes:** receipts, verification, evidence states, temporal validity, auditability.

**Annotation.** Project Constellation formalizes a distinction between discovered work, unverified implementation, tested builds, release candidates, deployments, and verified live behavior. Evidence must be bound to an exact revision, environment, check, time, and result. A new failed or unrun test can invalidate a previously recorded pass for that check. The document explicitly warns that a validator can check a receipt's structure without proving its truth. This paper is especially valuable for moving from compelling narratives about agentic productivity to falsifiable operational claims.

**Critical question:** Can external evaluators reproduce a representative sample of the release receipts and confirm that status transitions reject unsupported promotions?

### B07. Intention Semantics and the ChatGPT Exchange
**Source:** [`artificial-continuity/docs/INTENTIONS_AND_CHATGPT_BRIDGE.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/INTENTIONS_AND_CHATGPT_BRIDGE.md)  
**Type:** Human-AI workflow and approval protocol. **Status:** Inspected specification.  
**Themes:** intent capture, human review, progress truthfulness, model boundaries.

**Annotation.** This document specifies a manually reviewed exchange in which a user prepares a bounded intention, sends it to an assistant, receives structured proposed changes, compares them against the current baseline, and selects what to save. No proposal is approved simply because a model generated valid JSON. It distinguishes barriers, prerequisites, genuine waiting conditions, and next actions under human control. The separation is useful for avoiding false progress reports and inflated claims of automation.

**Critical question:** What user-experience tradeoffs emerge from explicit review when the number of active intentions grows large?

### B08. Context Consent Receipts
**Source:** [`artificial-continuity/docs/CONTEXT_CONSENT.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/CONTEXT_CONSENT.md)  
**Type:** Privacy architecture / receipt schema. **Status:** Inspected design.  
**Themes:** data minimization, consent, external model access, traceability.

**Annotation.** This design records metadata describing a bounded outbound context request, including provider, purpose, scope policy, approximate size, identifiable entity IDs, timestamp, and payload hash. The receipt deliberately avoids storing the full sensitive text a second time. It can help answer what context was prepared for transmission, but cannot prove what a remote service subsequently did. That limitation is essential: evidence of a request is not evidence of downstream provider behavior.

**Critical question:** How can a user verify redaction quality, retention promises, and downstream processing without relying solely on vendor statements?

### B09. Continuity Family: Implementation Boundary
**Source:** [`artificial-continuity/docs/FAMILY_ARCHITECTURE.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/FAMILY_ARCHITECTURE.md)  
**Type:** Product-family consolidation / scope boundary. **Status:** Inspected.  
**Themes:** source capture, typed provenance, product architecture, data ownership.

**Annotation.** This document clarifies that Continuity, Total Recall, MindVault/EchoLens, and Intent Integrity name different capabilities or historical branches, not automatically separate production systems. It distinguishes text input, manual transcription, OCR, and source exports by evidentiary strength; an imported transcript is not proof that a microphone recorded audio. It also insists that saved observations cannot become confirmed decisions or external-action permissions merely through ingestion. For the atlas, it is a useful guard against turning a vocabulary of ambitious project names into a fictitious inventory of working products.

**Critical question:** What single, current capability matrix accurately distinguishes prototypes, tests, live integrations, and research-only features?

### B10. Living Archive: Private Messenger Evidence
**Source:** [`artificial-continuity/docs/LIVING_ARCHIVE.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/docs/LIVING_ARCHIVE.md)  
**Type:** Archive and provenance interface specification. **Status:** Inspected.  
**Themes:** source witnesses, private archives, interpretation boundaries, versioning.

**Annotation.** This design describes an additive source-preserving archive for private message exports. It distinguishes original file hashes, decoded text hashes, source message identity, prior projections, and owner-reviewed interpretations. It warns that repeated copies do not create independent corroboration, and that imported text is evidence rather than an instruction. The paper is relevant to a comprehensive mind journal precisely because one must preserve a source without pretending its existence establishes authorship, factual truth, or consent for public exposure.

**Critical question:** Can an archive migration prove that all source-to-derivative mappings survive lossless export and recovery?

### B11. Artificial Continuity Project README
**Source:** [`artificial-continuity/README.md`](https://github.com/Noahhawkes/artificial-continuity/blob/main/README.md)  
**Type:** Product and release overview. **Status:** Inspected at version 0.22.1; mutable default-branch reference.  
**Themes:** local-first application, reviewed audio, manual model handoff, human agency.

**Annotation.** The README presents a local-first continuity workspace and documents the distinction between a manual ChatGPT exchange and a direct account integration. It says the browser database is not encrypted and does not automatically synchronize across devices. It is valuable as a snapshot of claims and declared limitations, but future edits can change this source. Release claims should be cross-checked against the exact commit before being treated as historical facts.

**Critical question:** Which user journeys have physical-device and cross-session recovery evidence at this version?

## Related repositories and research context

These are **repository-level pointers**, not assertions that every document inside is an original Hawkes publication:

- [Noahhawkes/artificial-continuity](https://github.com/Noahhawkes/artificial-continuity): primary inspected source set for this first edition.
- [Noahhawkes/oracle-ai-runtime](https://github.com/Noahhawkes/oracle-ai-runtime): related runtime lineage; article-by-article review pending.
- [Noahhawkes/oracle-ai-core](https://github.com/Noahhawkes/oracle-ai-core): related core architecture; article review pending.
- [Noahhawkes/LifeOS](https://github.com/Noahhawkes/LifeOS): large software and documentation repository; specific article inventory pending.
- [Noahhawkes/ai](https://github.com/Noahhawkes/ai): large software repository; specific article inventory pending.
- [Noahhawkes/ATANT](https://github.com/Noahhawkes/ATANT): relevant continuity-evaluation materials; its inspected standard names Samuel Sameer Tanguturi and Kenotic Labs in the byline. Keep it as a **separately attributed research source pending reconciliation**, not as proof one way or another of authorship of other files.
- [Noahhawkes/know-thyself](https://github.com/Noahhawkes/know-thyself): provenance-tagged personal knowledge graph material that refers to external project origins; useful comparative research, but origin and contribution level require document-level review.
- [Noahhawkes/memory](https://github.com/Noahhawkes/memory), [Noahhawkes/open-self](https://github.com/Noahhawkes/open-self): additional continuity-adjacent technical material; not yet classified article by article.

## Bibliographic priorities for the next revision

1. Enumerate every eligible Markdown, HTML, PDF, DOCX, and research-text file across the applicable repositories and branches.
2. Extract actual document titles, declared authors, dates, current and immutable revision links, word counts, abstract candidates, and document type.
3. Deduplicate mirrored articles by content hash while preserving every hosting URL and provenance record.
4. Tag original publication, derivative, collaboration, external citation, mirror, software documentation, and uncertain origin **without assuming repository ownership settles the question**.
5. Link each document to one or more of the fifty theme records and identify contradictory or superseding arguments.
6. Audit every citation target, create commit-pinned historical references, and separate reviewed conclusions from speculation.
7. Compare substantive claims against external literature, with sources and dates, before making novelty or priority assertions.

**Integrity note:** The bibliography will grow. The numbered records B01–B11 identify *inspected documents*, not a claim that only eleven articles exist.