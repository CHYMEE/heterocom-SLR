# Journal targeting and review exemplars

## What makes a strong venue for this review

There is no universally “best SLR journal.” Venue choice should follow the paper's main contribution, journal scope, article-type policy, audience, review expectations, and the authors' publication constraints. Journal metrics alone do not establish fit or acceptance prospects. The journal's live author instructions should be checked immediately before submission; review-article policies and special calls can change.

The paper can be positioned as a researcher-facing, evidence-based review of heterogeneous-compression FL and blockchain-supported integrity for resource-constrained IIoT. The distinctive synthesis is the operationally defined five-capability matrix, conservative consensus scoring, and concrete design guidance. This distinction must be shown against earlier nearby reviews rather than asserted from the empty capability intersection alone.

## Recommended submission sequence

| Priority | Candidate | Why it may fit | Main condition / risk |
|---|---|---|---|
| 1 | **IEEE Access** | Closest topical precedent: it published a systematic review combining fog computing, blockchain, federated learning, and IoT applications in 2024. The broad engineering readership is compatible with a cross-cutting, evidence-matrix review. | Explicitly differentiate from the 2024 review and explain why the narrower five-capability evaluation adds new evidence and researcher value. Check current survey/review article requirements, scope, fees, length limits, and reporting checklist. |
| 2 | **Journal of Parallel and Distributed Computing** | Stronger option if the paper foregrounds distributed-learning systems, resource-aware computation, compression, and aggregation/convergence under heterogeneity. It published a systematic review on resource-optimizing FL for IoT in 2023. | The paper needs deeper technical synthesis of aggregation assumptions and resource trade-offs, not just a PRISMA funnel and gap-count table. Confirm the current journal accepts this review type. |
| 3 | **IEEE Internet of Things Journal** | Potential fit if the narrative emphasizes industrial device heterogeneity, edge deployment, testbeds, and practical implications for IIoT. | A review that is mainly blockchain protocol or theoretical FL may be too diffuse. Verify current review/survey submission policy and whether the journal is soliciting such papers. |
| 4 | **International Journal of Communication Systems** | Possible alternative for a communications/networking framing with measured communication, latency, and resource overhead. It has published an SLR on FL-based IoT. | The manuscript should make network/system implications central; check current journal scope and article-type requirements. |

This is a fit-based shortlist, not a ranking of journal quality, impact factor, quartile, or likelihood of acceptance. Before choosing, compare the current journal scope, recently published reviews, article-type rules, length, open-access costs, indexing status required by the authors' institution/funder, and whether the journal allows a systematic review without meta-analysis.

## Closely related review papers to study

### 1. Closest topical precedent

Solis, W. V., Parra-Ullauri, J. M., and Kertész, A. “Exploring the Synergy of Fog Computing, Blockchain, and Federated Learning for IoT Applications: A Systematic Literature Review.” *IEEE Access*, vol. 12, pp. 68015–68060, 2024. [https://doi.org/10.1109/ACCESS.2024.3398034](https://doi.org/10.1109/ACCESS.2024.3398034).

**Why it matters:** its title and scope directly overlap the FL–blockchain–IoT intersection. Read this first and prepare a side-by-side comparison: review questions, search end date, databases, included primary-study set, treatment of system heterogeneity, compression selection, mismatched-model aggregation guarantees, metadata forgery, verification complexity, and hardware evaluation. Do not frame the current review as the first to connect these fields. Explain exactly what this review adds beyond an integrated fog/blockchain/FL survey.

**What to adapt:** clear taxonomy, a readable system-level framing, and a dedicated research-challenges discussion. **What to improve for this manuscript:** publish reproducible search strings and screening criteria, distinguish primary evidence from secondary surveys, state operational coding rules, and connect each gap claim to the study-level extraction matrix.

### 2. FL resource-optimization review

Ferreira da Silva, L. G., Sadok, D. F. H., and Endo, P. T. “Resource optimizing federated learning for use with IoT: A systematic review.” *Journal of Parallel and Distributed Computing*, vol. 175, pp. 92–108, 2023. [https://doi.org/10.1016/j.jpdc.2023.01.006](https://doi.org/10.1016/j.jpdc.2023.01.006).

**Why it matters:** a useful model for organizing resource-optimization strategies in FL/IoT. Compare its taxonomy and treatment of efficiency metrics with the current matrix's device-profile-driven compression, hardware tiers, communication, and memory evidence.

### 3. Broader FL-IoT SLR

Hosseinzadeh, M., Hemmati, A., and Rahmani, A. M. “Federated learning-based IoT: A systematic literature review.” *International Journal of Communication Systems*, vol. 35, no. 11, 2022. [https://doi.org/10.1002/dac.5185](https://doi.org/10.1002/dac.5185).

**Why it matters:** a broader FL-IoT review that can help contextualize earlier taxonomies and motivate the need for an updated, narrower synthesis. The current review's 2026 search period and explicit cross-domain capability coding should be contrasted carefully with its scope and search end date.

## Recommended positioning

The main contribution should be the evidence synthesis and its practical research agenda—not a claim that the empty intersection proves a new architecture is necessary or already validated. A defensible contribution statement is:

> This review operationalizes and compares five capabilities spanning live-resource compression, aggregation guarantees under model-size mismatch, metadata-forgery defenses, constant-complexity verification, and heterogeneous hardware evaluation. Across 293 included primary studies, the consensus coding found no study satisfying the complete capability set and no study coded Yes for the first two capabilities. The review uses this evidence to identify research and reporting priorities within its stated search and eligibility scope.

The contribution is substantially stronger if the Results section provides, for each research question, a countable taxonomy and representative study-level examples from the workbook, including counterexamples and Partial scores. Explain the boundary between the review and the 2024 IEEE Access SLR explicitly in the Introduction or a “Related reviews and contribution” subsection.

## Reporting standards and submission checks

- Use the [PRISMA 2020 checklist and flow diagram](https://www.prisma-statement.org/prisma-2020) for review reporting.
- Use [PRISMA-S](https://doi.org/10.1186/s13643-020-01542-z) to report each information source, exact query, search date, limits, deduplication, and supplementary search.
- Include the completed checklist and database-specific search strategies as supplements if the selected journal permits.
- Do not claim “best,” “first,” “comprehensive,” or “all relevant studies” without defining and substantiating the claim.
