# Review methods and audit trail

## Review question and scope

This review synthesizes primary research on heterogeneous-compression federated learning (FL) and blockchain-based integrity verification for resource-constrained industrial Internet of Things (IIoT) settings. Its PICOC scope is:

- **Population:** resource-constrained IIoT devices spanning different compute capabilities.
- **Intervention:** heterogeneous or adaptive model compression in FL, considered with blockchain-based integrity or trust verification.
- **Comparison:** uniform compression, standard robust aggregation, and conventional full-logging blockchain integration.
- **Outcomes:** compression, convergence or accuracy, Byzantine/metadata-forgery detection, and blockchain gas, latency, or memory overhead.
- **Context:** real or simulated resource-constrained industrial IoT; generic IoT and data-center FL without that context were outside scope.

The review questions cover compression-ratio selection, aggregation across mismatched model sizes, metadata-forgery threats, constant-complexity on-chain verification and its overhead, and combinations of these capabilities. Hardware/system heterogeneity is distinguished from statistical data heterogeneity (for example, non-IID client data).

## Sources and search period

The recorded data-collection period was July 1–September 1, 2026. Searches covered IEEE Xplore, the ACM Digital Library, Google Scholar, Web of Science, and Scopus. The aggregate identification count used in the review is 4,475. The collection summary lists the following source yields; verify them against the original database exports before submission:

| Source | Records |
|---|---:|
| IEEE Xplore | 1,566 |
| ACM Digital Library | 686 |
| Google Scholar | 866 |
| Web of Science | 636 |
| Scopus | 721 |
| **Total** | **4,475** |

Backward reference-list checking and forward citation searching (snowballing) were performed. The reviewers report that citation searching yielded **no additional eligible studies beyond the identified set**.

Search concepts combined synonyms for FL, model compression/heterogeneity, blockchain/integrity verification, and industrial/resource-constrained IoT, with database-specific syntax. The exact executed query for each source and the exact per-source run date should be copied from the original database search histories or Zotero export log into the supplementary search strategy; they are not reconstructed here.

The aggregate count and source-level yields above are transcribed from the collection summary. The aggregate reconciles with the documented deduplication and screening flow, but the per-source yields still require verification against the original exports. The review therefore uses 4,475 as the aggregate identification count and does not infer a source-level correction without export provenance.

## Eligibility

Studies published from 2022 through the search period were eligible when they were peer-reviewed journal or top-tier conference primary studies, addressed at least two of heterogeneous compression, FL aggregation under mismatch, blockchain integrity/trust, and IIoT resource constraints, and reported at least one quantitative outcome relevant to the PICOC outcomes.

Exclusions included pre-2022 or non-English studies; inaccessible full texts; records without a peer-reviewed version; uniform-compression-only studies without a heterogeneity dimension; generic IoT or data-center FL without the required industrial/resource-constrained context; blockchain used only as a ledger or log without verification logic; and secondary studies. Surveys and reviews were kept separately as related literature, not included in the primary evidence set. At full text, each excluded study was assigned a reason.

## Record management and screening

1. Search results were managed in Zotero, with source-specific collections.
2. The collection record reports that Zotero duplicate detection identified 2,221 items and 1,346 items were deleted on September 16–17, 2026. The Zotero export contained 3,129 records. On September 18, Rayyan identified 26 further duplicates; 12 were deleted, leaving 3,117 records. The exact matching rules used by either tool are not documented.
3. Two reviewers screened records independently in Rayyan with blind mode enabled. Title-only screening ran from September 23 through October 7, 2026: 2,402 records were retained and 715 excluded.
4. Abstract screening ran from October 8 through 18, 2026: 331 records were retained and 2,071 excluded.
5. During reviewer reconciliation, eight of the 331 records retained after abstract screening were determined ineligible before full-text assessment. Thus, 2,786 records were excluded at title/abstract screening and eight more at reconciliation, for 2,794 exclusions and 323 full texts assessed. Full texts were independently assessed by two reviewers, with exclusion reasons recorded. The project reports 28 decision conflicts resolved.
6. Citation searching was performed; it added no eligible studies beyond the identified set.
7. Inter-rater agreement was calculated before consensus resolution: title/abstract Cohen's κ approximately 0.61, with approximately 91% raw agreement over 3,117 records; full-text inclusion κ = 0.615, with 92.5% raw agreement over 319 paired decisions. Four of the 323 full-text decisions lacked paired independent ratings and therefore were not in the kappa calculation; they remained in the final selection decisions.

### Locked PRISMA counts

| Stage | Count |
|---|---:|
| Records identified in databases | 4,475 |
| Duplicates removed in Zotero | 1,346 |
| Additional duplicates removed in Rayyan | 12 |
| Records screened by title/abstract | 3,117 |
| Title-only exclusions | 715 |
| Abstract-stage exclusions | 2,071 |
| Additional records determined ineligible during reconciliation | 8 |
| Total exclusions before full-text assessment | 2,794 |
| Full texts assessed | 323 |
| Full-text exclusions | 30 |
| Studies included in synthesis | 293 |

The counts reconcile: 4,475 − 1,346 − 12 = 3,117; 715 + 2,071 + 8 = 2,794; 3,117 − 2,794 = 323; and 323 − 30 = 293. Snowballing yielded no additional eligible studies. The full-text kappa denominator is 319 paired decisions, not the 323 full texts assessed.

## Full-text assessment and extraction in Excel

The reviewers used separate extraction/reconciliation workbooks and a final consensus workbook. The final matrix contains 293 included studies and records citation metadata; five capability scores; accuracy, F1, gas, latency, memory/overhead, and compression when reported; dataset; hardware/testbed; key contribution; and limitation. Values not reported by a paper were left blank rather than inferred.

Each capability was scored **Yes**, **Partial**, or **No** using these operational rules:

| Capability | Yes threshold / coding rule |
|---|---|
| Adaptive ratio from live resource profile | Compression is selected from current device state (e.g. CPU, RAM, battery); a fixed setting or only a preset tier is not sufficient. |
| Convergence-guaranteed aggregation | A proof or formal bound supports aggregation across differently sized submodels; empirical convergence alone is not Yes. |
| Metadata-forgery threat model | The method addresses a participant lying about contribution metadata (e.g. its claimed compression ratio); generic Byzantine or bad-weight detection alone is insufficient. |
| O(1) on-chain verification | Evidence supports constant verification cost as nodes grow and reports relevant overhead such as gas, latency, or memory. |
| Heterogeneous multi-tier evaluation | Yes requires at least two genuinely different physical hardware tiers; realistic simulated tiers are Partial. |

Reviewers scored capabilities independently. Where ordinal capability scores differed, the consensus adopted the more conservative (less complete) score. This rule yielded the final counts below:

| Capability | Yes | Partial | No | Yes (%) |
|---|---:|---:|---:|---:|
| Adaptive live-resource compression | 0 | 1 | 292 | 0% |
| Convergence-guaranteed aggregation | 0 | 8 | 285 | 0% |
| Metadata-forgery threat model | 2 | 26 | 265 | 1% |
| O(1) on-chain verification | 3 | 21 | 269 | 1% |
| Heterogeneous multi-tier evaluation | 16 | 23 | 254 | 5% |

No included paper satisfied all five capabilities; the consensus summary also records zero papers satisfying at least three, four, or all five.

**Percentage reconciliation:** the supplied results image labels the last row as 7%, but the locked numerator and denominator give 16/293 = 5.46%, which rounds to **5%** to the nearest whole percentage point. The workbook and manuscript consistently use 5%; the 7% in that image is treated as a calculation/label error unless the underlying study count or denominator is revised.

## Tool roles

- **Zotero:** reference collection, source-specific organization, and duplicate management.
- **Rayyan:** independent, blind title/abstract screening and reviewer decision tracking.
- **Microsoft Excel:** full-text extraction, eligibility/reason reconciliation, capability coding, consensus matrix, descriptive counts, and PRISMA/kappa summaries.
- **HiTeX and GitHub:** manuscript drafting and version history. These are writing/reproducibility tools, not screening or eligibility adjudication tools.

Software versions and the exact Zotero duplicate-detection settings are not recorded in the materials inspected and should be added if recoverable.

## Items to verify before submission

- Attach a supplementary file containing the exact query string and run date for each source, copied from the actual search histories; do not recreate queries from memory.
- Retain/export the Zotero deduplication report or document whether duplicate removal combined automatic matching with manual review.
- Preserve the source exports supporting the 4,475 aggregate identification count and verify each per-source yield before submission; do not revise source-level totals without export provenance.
- Confirm whether a formal risk-of-bias/study-quality assessment was conducted. No separate appraisal instrument was documented in the reviewed project files.
- Complete the PRISMA 2020 checklist and PRISMA-S search-reporting checklist; link each item to its manuscript location or supplementary material.
- Confirm team author names/affiliations and journal-specific review article requirements before submission.

## Core reporting references

- Page MJ, McKenzie JE, Bossuyt PM, et al. The PRISMA 2020 statement: an updated guideline for reporting systematic reviews. *BMJ*. 2021;372:n71. <https://doi.org/10.1136/bmj.n71>.
- Rethlefsen ML, Kirtley S, Waffenschmidt S, et al. PRISMA-S: an extension to the PRISMA Statement for Reporting Literature Searches in Systematic Reviews. *Systematic Reviews*. 2021;10:39. <https://doi.org/10.1186/s13643-020-01542-z>.
