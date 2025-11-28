# CRISPR-Cas9-Single-Guide-RNA-sgRNA-Design-and-Genomic-Validation-for-Human-TNF-Gene-Knock-out
CRISPR/Cas9 Single-Guide RNA (sgRNA) Design and Genomic Validation for Human TNF Gene Knock-out
# CRISPR/Cas9 Single-Guide RNA (sgRNA) Design for Knock-out of Human TNF Gene

### 🧬 Project Overview

This repository documents the target site selection process for a CRISPR/Cas9-mediated **gene knock-out** targeting the human **Tumor Necrosis Factor (TNF)** gene, which is a critical inflammatory cytokine. The analysis was conducted using the CHOPCHOP design tool (targeting *Homo sapiens*, genome assembly GRCh38).

***

### 🔬 Genomic Context (UCSC Genome Browser Analysis)

The genomic context derived from the UCSC Genome Browser confirms the structural characteristics of the *TNF* gene. 

* **Genomic Coordinates:** The analysis window covers **chr6:31,575,564-31,578,335** (approximately 2.77 kb).
* **Transcript Structure:** The *TNF* gene is transcribed on the **minus strand** (reverse orientation). The target site is located within a **coding exon**, which is optimal for inducing a functional knock-out.

***

### 🎯 Key Findings: Optimal sgRNA Target Site

The search identified highly specific and efficient single-guide RNA (sgRNA) candidates.

| Rank | Target Sequence (5' to 3') | PAM | Genomic Location | Strand | Efficiency Score |
| :---: | :--- | :--- | :--- | :---: | :---: |
| **1** | **GCCAGAGGGCCTGTACCTGA** | **AGG** | chr6:31577747 | - | 72.82% |
| **2** | **TCTGGGCAAGGGGCTGGGGG** | **GGG** | chr6:31577732 | - | **80.35%** |

*Note: Rank 2 exhibits the highest predicted on-target cleavage efficiency at 80.35%, indicating a high potential for successful cutting.*

#### **Specificity (Off-Target Analysis for Rank 1)**

The Rank 1 sgRNA sequence is highly specific, showing **zero** predicted off-target matches with up to two mismatches (MM) found in the reference genome.

| Off-Target Mismatches (MM) | Count |
| :---: | :---: |
| **Perfect Matches (MM0)** | **0** |
| **1 Mismatch (MM1)** | **0** |
| **2 Mismatches (MM2)** | **0** |
| 3 Mismatches (MM3) | 2 |

#### **Predicted Knock-out Outcome (Repair Profile for Rank 1)**

The predicted repair profile (Shen et al. 2018 predictions) for the Rank 1 site is highly favorable for generating a functional knock-out via Non-Homologous End-Joining (NHEJ).

| Metric | Predicted Value | Interpretation |
| :--- | :--- | :--- |
| **Frameshift Frequency** | **67.11%** | A high probability of achieving a successful gene-inactivating frame-shift mutation. |
| **Highest Deletion Frequency**| **76.51%** | The most frequent single repair outcome, which simplifies clone screening. |
| **Microhomology Deletion** | **89.26%** | Very high frequency indicating predictable deletion patterns. |

***

### 🔬 Validation Strategy: PCR Primers

The tool designed a highly specific PCR primer pair for validating the editing success at the Rank 1 target site.

* **Primer Specificity:** The recommended pair has **0** predicted off-targets.
* **Product Size:** 257 bp (optimal for standard validation assays).

| Pair | Left Primer (5' to 3') | Right Primer (5' to 3') | Product Size |
| :---: | :--- | :--- | :---: |
| **4** (Recommended) | `GACGTGGCCAGAGGGCC` | `ACCCACTTCAGCAGCTTGC` | 257 bp |

***

### 📂 File Structure

| File Name | Content |
| :--- | :--- |
| `TNF gRNA_Screening_Summary.html` | The comprehensive, ranked list of all identified sgRNA candidates, including core specificity metrics and efficiency scores. |
| `TNF_Rank1_gRNA_Detail_Analysis.html` | The in-depth breakdown for the top-ranked sgRNA, containing target visualization, predicted NHEJ repair statistics, and validation primer details. |
| `TNF Human hg38 chr6：31575564-31578335 UCSC Genome Browser v490 .html` | UCSC Genome Browser track visualization confirming the *TNF* gene structure and location within the hg38 assembly. |
