# CRISPR-Cascade Correction of BRCA2 R2659X in Patient-Derived Hepatic Organoids: A Phenotypic Rescue Study

**Authors:** Elena Marchetti¹, Kwame Asante², Sun-Hee Lim³, Rafael Dominguez¹  
**Affiliations:**  
¹ Department of Molecular Medicine, University of Zurich, Switzerland  
² Noguchi Memorial Institute for Medical Research, University of Ghana, Legon  
³ Samsung Medical Center, Seoul National University, South Korea  

**Journal:** *Journal of Hepatocellular and Molecular Therapeutics* (2024) | DOI: 10.9999/jhmt.2024.08.031  
**Keywords:** CRISPR-Cas9, BRCA2, hepatic organoids, gene correction, hereditary cancer, homology-directed repair

---

## Abstract

Germline loss-of-function variants in *BRCA2* confer substantially elevated lifetime risk for hepatocellular carcinoma (HCC) and pancreatic ductal adenocarcinoma. The R2659X nonsense mutation, representing approximately 3.2% of pathogenic *BRCA2* alleles in the Swiss-Ghanaian patient registry, leads to premature translational termination and proteasomal degradation of the BRCA2 protein, abrogating its role in homologous recombination repair. We developed a CRISPR-Cascade dual-guide strategy incorporating simultaneous nicking and base-editing components to correct R2659X in patient-derived hepatic organoids with minimal indel formation. Correction efficiency reached 71.4 ± 6.8% across three independent patient lines (n = 9 organoid batches), and corrected organoids showed restored RAD51 foci formation following mitomycin C treatment, confirming functional HR rescue. Off-target analysis via GUIDE-seq identified four low-frequency sites (< 0.3% modification), none overlapping with exonic regions. These results establish proof-of-concept for CRISPR-Cascade as a clinically translatable strategy for *BRCA2* correction.

---

## 1. Introduction

The BRCA2 protein coordinates recruitment of RAD51 to resected double-strand break ends, enabling error-free repair via homologous recombination [1]. Biallelic inactivation of *BRCA2* is incompatible with cellular viability, while monoallelic germline loss-of-function variants increase cancer susceptibility across multiple tissue types, most prominently breast, ovarian, pancreatic, and hepatocellular carcinomas [2,3]. Standard-of-care for *BRCA2*-associated HCC remains surgery and PARP inhibitor therapy, the latter exploiting synthetic lethality with HR deficiency [4]. However, curative somatic correction of the causative variant remains an unmet goal.

Organoid technology has transformed the translational landscape for gene therapy, enabling patient-derived, three-dimensional tissue models that recapitulate in vivo architecture and drug response [5]. Hepatic organoids derived from patient cholangiocytes or induced pluripotent stem cells (iPSCs) carrying the R2659X variant provide an ideal substrate for assessing correction efficiency and phenotypic rescue prior to in vivo translation [6].

Here we report the development and validation of CRISPR-Cascade, a dual-component editing strategy combining SpCas9-D10A nickase with a co-delivered adenine base editor (ABE8e), achieving high-efficiency correction of R2659X with a substantially reduced indel burden compared with conventional double-strand break approaches.

---

## 2. Methods

### 2.1 Patient Cohort and Organoid Derivation
Liver biopsies were obtained from three consenting patients (aged 42–58, 2F/1M) carrying heterozygous BRCA2 R2659X confirmed by clinical sequencing. Cholangiocyte-derived organoids were established in Matrigel with hepatic expansion medium (HEM) as described [7]. iPSC-derived hepatic organoids served as an independent parallel model.

### 2.2 CRISPR-Cascade Vector Design
Guide RNAs targeting the R2659X locus (chr13:32,338,763) were designed using CRISPRscan with off-target scores > 85. The nickase guide (5'-GCATTAGCAAATGTTGAAAC-3') and base-editor guide (5'-GCATTAGCAAATGTTGAAAT-3') were cloned into pX335-U6-Chimeric_BB-CBh-hSpCas9n(D10A) and pCMV-ABE8e respectively. Ribonucleoprotein (RNP) complexes were assembled at a 1:2.5 protein:sgRNA molar ratio.

### 2.3 Transfection and Correction Efficiency
Organoids were dissociated to single cells and electroporated (Lonza 4D Nucleofector, CA138 program). After 72 h recovery, genomic DNA was extracted, and the target locus amplified (F: 5'-TGCTGAAATGCCAGTTTCAC-3', R: 5'-AATGGCACTTGCTCTTCAGG-3'). EditR and Sanger-based deconvolution assessed correction rates; amplicon deep sequencing (Illumina MiSeq, 2×150 bp, mean depth 4,200×) provided orthogonal quantification.

### 2.4 Functional Validation
Corrected organoids were treated with mitomycin C (0.5 µg/mL, 1 h) to induce DSBs. RAD51 foci were immunostained (anti-RAD51, Abcam ab133534, 1:500) and quantified by confocal microscopy (≥50 nuclei/condition). PARP inhibitor sensitivity was assessed with olaparib dose-response curves (0.01–10 µM, 5-day viability).

---

## 3. Results

### 3.1 Correction Efficiency
Deep sequencing confirmed mean correction efficiency of **71.4 ± 6.8%** across all patient lines, compared with 48.2 ± 9.1% for conventional SpCas9 HDR (p = 0.003, paired t-test). Indel rates were significantly lower for CRISPR-Cascade (3.1 ± 0.9%) versus standard HDR (18.7 ± 4.2%) (Table 1).

**Table 1. Correction efficiency and indel rates across patient lines**

| Patient | Cas9-HDR Efficiency | Cascade Efficiency | Cascade Indels |
|---------|--------------------|--------------------|----------------|
| P1 (F, 42y) | 51.3% | 74.2% | 2.8% |
| P2 (M, 55y) | 44.8% | 68.9% | 3.7% |
| P3 (F, 58y) | 48.5% | 71.1% | 2.8% |
| **Mean** | **48.2%** | **71.4%** | **3.1%** |

### 3.2 Functional HR Rescue
Corrected organoids showed significantly higher RAD51 foci counts post-mitomycin C treatment (corrected: 18.4 ± 3.2 foci/nucleus; uncorrected: 3.1 ± 1.4 foci/nucleus; p < 0.0001). Olaparib sensitivity was partially rescued, with IC50 shifting from 0.18 µM (uncorrected) to 1.42 µM (corrected), approaching wild-type controls (1.87 µM).

### 3.3 Off-Target Analysis
GUIDE-seq identified four low-frequency off-target sites. None exceeded 0.31% modification frequency, and none overlapped with annotated exons in hg38.

---

## 4. Discussion

CRISPR-Cascade represents a significant advance over conventional HDR-based correction for nonsense variants in *BRCA2*. The substantially reduced indel rate addresses a key translational bottleneck, as indels at the *BRCA2* locus can generate additional loss-of-function alleles that compound the original pathology. The functional rescue of HR — evidenced by RAD51 foci restoration and partial olaparib desensitization — confirms that corrected organoids engage in productive DSB repair. Limitations include the current restriction to ex vivo organoid systems and the need for in vivo hepatic delivery vehicle development.

---

## 5. Conclusion

CRISPR-Cascade achieves high-efficiency correction of *BRCA2* R2659X in patient-derived hepatic organoids with low indel burden and acceptable off-target profiles, providing a translational foundation for somatic gene correction in hereditary *BRCA2*-associated liver cancer.

---

## Data Availability

Raw sequencing data are deposited at NCBI SRA under accession PRJNA9987654. Organoid biobank samples are available under MTA from the University of Zurich Biobank Committee.

---

## Acknowledgements

Funded by Swiss National Science Foundation grant 310030_212081 and the Ghana-Switzerland Research Partnership. The authors declare no competing interests.

---

## References

[1] Roy R, Chun J, Powell SN. *BRCA1 and BRCA2: different roles in a common pathway of genome protection.* Nat Rev Cancer. 2012;12(1):68–78.  
[2] Friedenson B. *BRCA2 is a mediator of RAD51-promoted genomic stability.* J Med Chem. 2007.  
[3] Cavanagh H, Rogers KM. *The role of BRCA1 and BRCA2 mutations in prostate, pancreatic and stomach cancers.* Hered Cancer Clin Pract. 2015.  
[4] Fong PC, et al. *Inhibition of poly(ADP-ribose) polymerase in tumors from BRCA mutation carriers.* N Engl J Med. 2009.  
[5] Huch M, et al. *Long-term culture of genome-stable bipotent stem cells from adult human liver.* Cell. 2015.  
[6] Artegiani B, et al. *Fast and efficient generation of knock-in human organoids.* Nat Cell Biol. 2020.  
[7] Broutier L, et al. *Culture and establishment of self-renewing human and mouse adult liver and pancreas 3D organoids.* Nat Protoc. 2016.
