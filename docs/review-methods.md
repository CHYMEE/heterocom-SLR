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

The recorded data-collection period was July 1–September 1, 2026. Searches covered IEEE Xplore, the ACM Digital Library, Google Scholar, Web of Science, and Scopus. The final locked database-record counts are:

| Source | Records |
|---|---:|
| IEEE Xplore | 1,565 |
| ACM Digital Library | 686 |
| Google Scholar | 829 |
| Web of Science | 636 |
| Scopus | 721 |
| **Total** | **4,437** |

Backward reference-list checking and forward citation searching (snowballing) were performed. The reviewers report that citation searching yielded **no additional eligible studies beyond the 4,437-record set**.

Search concepts combined synonyms for FL, model compression/heterogeneity, blockchain/integrity verification, and industrial/resource-constrained IoT, with database-specific syntax. The exact executed query for each source and the exact per-source run date should be copied from the original database search histories or Zotero export log into the supplementary search strategy; they are not reconstructed here.

## Eligibility

Studies published from 2022 through the search period were eligible when they were peer-reviewed journal or top-tier conference primary studies, addressed at least two of heterogeneous compression, FL aggregation under mismatch, blockchain integrity/trust, and IIoT resource constraints, and reported at least one quantitative outcome relevant to the PICOC outcomes.

Exclusions included pre-2022 or non-English studies; inaccessible full texts; records without a peer-reviewed version; uniform-compression-only studies without a heterogeneity dimension; generic IoT or data-center FL without the required industrial/resource-constrained context; blockchain used only as a ledger or log without verification logic; and secondary studies. Surveys and reviews were kept separately as related literature, not included in the primary evidence set. At full text, each excluded study was assigned a reason.

## Record management and screening

1. Search results were managed in Zotero, with source-specific collections visible in the project records.
2. The locked flow records 4,437 identified records and 1,320 duplicates removed, leaving 3,117 records for title/abstract screening.
3. Two reviewers screened titles and abstracts independently and blind to each other's decisions in Rayyan. Clearly out-of-scope records were excluded; uncertain records were retained for closer review.
4. Full texts were assessed independently by two reviewers against the inclusion criteria, with exclusion reasons recorded.
5. Reviewer disagreements were resolved through reconciliation. The project reports 28 decision conflicts resolved. The final title/abstract exclusion total includes eight further exclusions settled during reconciliation.
6. Citation searching was performed; it added no eligible studies beyond the locked search set.
7. Inter-rater agreement was calculated before consensus resolution: title/abstract Cohen's κ approximately 0.61, with approximately 91% raw agreement over 3,117 records; full-text inclusion κ = 0.615, with 92.5% raw agreement over 319 paired decisions. Four of the 323 full-text decisions lacked paired independent ratings and therefore were not in the kappa calculation; they remained in the final selection decisions.

### Locked PRISMA counts

| Stage | Count |
|---|---:|
| Records identified in databases | 4,437 |
| Duplicates removed | 1,320 |
| Records screened by title/abstract | 3,117 |
| Title/abstract exclusions after reconciliation | 2,794 |
| Full texts assessed | 323 |
| Full-text exclusions | 30 |
| Studies included in synthesis | 293 |

The counts reconcile: 4,437 − 1,320 = 3,117; 3,117 − 2,794 = 323; and 323 − 30 = 293. Snowballing yielded no additional eligible studies. The full-text kappa denominator is 319 paired decisions, not the 323 full texts assessed.

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

**Percentage check:** the supplied results image labels the last row as 7%. However, 16/293 = 5.46%, which rounds to 5% to the nearest whole percentage point. The workbook and manuscript use the mathematically consistent 5%; change this only if the underlying numerator or denominator is corrected.

## Tool roles

- **Zotero:** reference collection, source-specific organization, and duplicate management.
- **Rayyan:** independent, blind title/abstract screening and reviewer decision tracking.
- **Microsoft Excel:** full-text extraction, eligibility/reason reconciliation, capability coding, consensus matrix, descriptive counts, and PRISMA/kappa summaries.
- **HiTeX and GitHub:** manuscript drafting and version history. These are writing/reproducibility tools, not screening or eligibility adjudication tools.

Software versions and the exact Zotero duplicate-detection settings are not recorded in the materials inspected and should be added if recoverable.

## Items to verify before submission

- Attach a supplementary file containing the exact query string and run date for each source, copied from the actual search histories; do not recreate queries from memory.
- Retain/export the Zotero deduplication report or document whether duplicate removal combined automatic matching with manual review.
- Verify that the final search yield and per-source counts match the exported records. These are the locked final counts supplied by the review team.
- Reconcile the earlier collection screenshot, which shows 4,475 items and Google Scholar = 866, with the locked PRISMA flow of 4,437 and Google Scholar = 829. This methods record and the updated figure use the locked PRISMA counts; explain whether the difference reflects an earlier pre-filter total, a subsequent exclusion before screening, or a superseded count.
- Confirm whether a formal risk-of-bias/study-quality assessment was conducted. No separate appraisal instrument was documented in the reviewed project files.
- Complete the PRISMA 2020 checklist and PRISMA-S search-reporting checklist; link each item to its manuscript location or supplementary material.
- Confirm team author names/affiliations and journal-specific review article requirements before submission.

## Core reporting references

- Page MJ, McKenzie JE, Bossuyt PM, et al. The PRISMA 2020 statement: an updated guideline for reporting systematic reviews. *BMJ*. 2021;372:n71. <https://doi.org/10.1136/bmj.n71>.
- Rethlefsen ML, Kirtley S, Waffenschmidt S, et al. PRISMA-S: an extension to the PRISMA Statement for Reporting Literature Searches in Systematic Reviews. *Systematic Reviews*. 2021;10:39. <https://doi.org/10.1186/s13643-020-01542-z>.
