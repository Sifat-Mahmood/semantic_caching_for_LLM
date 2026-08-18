# Systematic Literature Review of Semantic Caching for LLM Inference

A systematic literature review of semantic caching techniques for large language model inference. We screened 87 candidate records down to a 66-paper corpus, organised into five clusters, and identify a central gap the field has not yet measured: energy cost.

## Abstract

Running inference with a large language model can be expensive in terms of both computation and resources. Semantic caching can reduce this cost by reusing previously generated responses for new queries with similar meanings. Research on semantic caching has grown rapidly since 2023, but no published review provides a systematic overview of the field. This paper reviews 66 papers selected from 87 identified records and organizes them into five main clusters. The review identifies five problems: unreliable similarity thresholds, lack of conversation context, incomplete solutions, unmeasured costs of improving reliability, and stale cached information. Across 18 papers reported, speedups range from 1.6 to 3.1 times, while improvements in average latency are generally larger than improvements in tail latency. The review also finds that current studies mainly focus on latency, accuracy, hit rate, and monetary cost, with very limited attention to energy use. Most importantly, none of the reviewed papers measures the energy cost of semantic caching against the energy cost of the LLM inference it replaces. This reveals an important research gap in green computing. Based on this finding, the review identifies three open questions about when se mantic caching can provide real energy savings, how cache hit rate affects those savings, and how caching overhead changes energy benefit. The master corpus, quality-appraisal data, and full reference list are available in an accompanying GitHub repository: (https://github.com/Sifat-Mahmood/semantic_caching_for_LLM.git)

## Repository contents

| File | Description |
|---|---|
| `Systematic_Literature_Review_of_Semantic_Caching_for_LLM_Inference.pdf` | Full review paper (pdf). |
| `LaTeX_Source_Compressed.zip` | LaTeX source, Overleaf-ready, including `references.bib`. |
| `PRISMA_FLOW_DIAGRAM.png` | PRISMA-style screening flow diagram (Figure 1 in the paper). |
| `SLR_of_SCLLM_Master_Corpus.xlsx` | Master corpus spreadsheet: all 87 records, screening decisions, quality-appraisal scores, and citation metadata. |
| `Presentation_slide_SLR-of-SCLLM.pdf` | Course presentation slides (PDF). |
| `Presentation_slide_SLR-of-SCLLM.pptx` | Course presentation slides (editable). |

The exact filename of the paper document may differ slightly from what is listed above. Check the repository's file list directly if it does not match.

## Corpus at a glance

| Stage | Count |
|---|---|
| Records identified (3 search rounds) | 87 |
| Set aside as background citations | 3 |
| Screened against inclusion/exclusion criteria | 84 |
| Excluded | 18 |
| Included in final corpus | 66 |

| Cluster | Name | n |
|---|---|---|
| A | Core LLM Semantic Caching | 26 |
| B | Adaptive Threshold / Eviction / Verification | 12 |
| C | Security & Reliability of Caching | 5 |
| D | Agentic / Domain-Specific Caching | 12 |
| E | KV-Cache / Prefix-Level Caching (contrast evidence) | 11 |

Quality-appraisal tier distribution across the 66 included papers: 9 High, 47 Moderate, 10 Low.

## Key findings

- Five patterns recur across the corpus: unreliable similarity thresholds, context-blind caching decisions, fixes that solve one problem and leave the next unaddressed, reliability gains with unmeasured cost, and understudied staleness.
- Eighteen papers report results precise enough to compare directly, revealing a practical speedup ceiling near 1.6 to 3.1 times and a consistent gap between mean and tail-latency improvements.
- Not one paper in the corpus measures the energy cost of semantic caching against the energy cost of the direct inference it replaces.

This review turns that last finding into three open questions for future work: under what conditions semantic caching produces a net energy saving once its own overhead is counted, whether a minimum viable hit rate exists below which caching costs more energy than direct inference, and whether a high hit rate can be trusted to imply high savings at all.

## Supplementary materials

Additional working files, including intermediate drafts and screening records, are available in the project's Google Drive folder:
[Google Drive](https://drive.google.com/drive/folders/1uJBY-Hts1qh3mBjJOlIY-8J6jH684ySs?usp=drive_link)

## Generative AI usage

Portions of this project's drafting, editing, corpus verification, and presentation preparation used Claude, a generative AI assistant developed by Anthropic. Full disclosure is included in the paper's Generative AI Usage Statement section, and the authors take full responsibility for the accuracy of the final submitted work.

## Course information

CSE 407, Summer 2026. Group 5.

Dept of CSE, EWU

## Contributors

- [Sifat-Mahmood](https://github.com/Sifat-Mahmood)
- [Kaniz-Reza](https://github.com/Kaniz-Reza)
- [Red-Ahmed](https://github.com/Red-Ahmed)
- [ahmedshafi-ctrl](https://github.com/ahmedshafi-ctrl) [SUPERVISOR]

