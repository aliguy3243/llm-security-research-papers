# TokenShift: Quantifying Semantic Drift in Autoregressive Language Model Embeddings Across Training Epochs

**Authors:** Ingrid Vasquez¹, Dmitri Sorokin², Ayaan Khan³, Lena Hoffmann²  
**Affiliations:**  
¹ Universidad Autónoma de Madrid, School of Computer Science, Spain  
² ETH Zurich, Institute for Machine Learning, Switzerland  
³ Indian Institute of Technology Bombay, Department of CSE, India  

**Journal:** *Computational Linguistics & NLP Research* (2024) | DOI: 10.9999/clnlp.2024.07.0112  
**Keywords:** semantic drift, embedding stability, language model training dynamics, representational change, anisotropy, probing classifiers

---

## Abstract

The internal representations of autoregressive language models evolve substantially across training epochs, yet systematic characterization of this semantic drift remains limited. We introduce **TokenShift**, a framework for quantifying representational change in transformer embeddings across checkpoints using three complementary measures: (1) cosine centroid displacement (CCD), tracking mean embedding trajectory; (2) isotropy coefficient (IC), measuring distribution geometry; and (3) probing accuracy decay (PAD), using frozen probing classifiers trained on early checkpoints to detect concept drift. Applied to 47 checkpoints of a 1.3B-parameter GPT-style model trained from scratch on the Pile, TokenShift reveals three distinct training phases: *rapid specialization* (steps 0–5K), *representation compression* (steps 5K–80K), and *semantic stabilization* (steps 80K–300K). Layer-wise analysis shows that lower layers stabilize early while upper layers continue drifting through phase 3. Cross-model comparison across four architectures (GPT-2, BLOOM-560M, OPT-1.3B, our custom 1.3B) reveals consistent phase patterns, suggesting training dynamics are architecture-agnostic. TokenShift provides actionable insights for checkpoint selection in continual learning and domain adaptation.

---

## 1. Introduction

Training dynamics of large language models (LLMs) — how their internal representations evolve from random initialization to convergence — remain poorly understood. Most training analyses focus on loss curves and downstream task performance, overlooking the geometric and semantic evolution of learned representations [1]. Understanding when and where representational stability is achieved has practical implications: early-checkpoint continual learning can exploit plasticity before representations calcify, while late-checkpoint adaptation leverages stable semantics with minimal catastrophic forgetting [2].

Prior work on representational geometry has established that LLM embeddings tend toward anisotropic distributions [3], and that probing classifiers can decode syntactic and semantic properties from intermediate representations [4]. However, these analyses are largely static (single checkpoint). TokenShift extends this to the temporal dimension, treating training as a dynamic process whose representational trajectory is itself a meaningful signal.

---

## 2. TokenShift Metrics

### 2.1 Cosine Centroid Displacement (CCD)
For layer $l$ and checkpoint $t$, the embedding centroid $\mu_t^l = \frac{1}{|V|}\sum_{v \in V} e_t^l(v)$. CCD between consecutive checkpoints: $\text{CCD}(t, t+1, l) = 1 - \cos(\mu_t^l, \mu_{t+1}^l)$.

### 2.2 Isotropy Coefficient (IC)
$\text{IC}_t^l = \frac{1}{|I|}\sum_{(i,j) \in I} \cos(e_t^l(w_i), e_t^l(w_j))$ — mean pairwise cosine similarity for a random sample of 10,000 token pairs. Lower IC → more isotropic (geometrically uniform).

### 2.3 Probing Accuracy Decay (PAD)
Train probing classifiers (linear SVM) on 15 semantic/syntactic tasks using representations from checkpoint $t_0$ (step 5K). Freeze classifier, evaluate at all subsequent checkpoints. PAD = accuracy drop relative to $t_0$.

---

## 3. Results

**Three training phases identified (1.3B model):**

| Phase | Step Range | CCD Magnitude | IC Trend | PAD |
|-------|-----------|---------------|----------|-----|
| Rapid Specialization | 0–5K | High (0.12–0.41) | Decreasing | Baseline |
| Representation Compression | 5K–80K | Medium (0.03–0.11) | Low/stable | 0–8% |
| Semantic Stabilization | 80K–300K | Low (< 0.02) | Slight increase | 8–15% |

Cross-architecture: all four models exhibit the same three-phase pattern (Spearman ρ = 0.89–0.94 between CCD curves after step normalization).

Layer-wise: layers 1–4 stabilize by step 20K; layers 8–12 continue drifting through step 150K.

---

## 4. Discussion

The representation compression phase (steps 5K–80K) is characterized by simultaneous high plasticity and rapid semantic reorganization — exactly the window most amenable to continual pre-training on domain-specific corpora without full fine-tuning. The stabilization phase, while semantically rigid, shows increased anisotropy that may contribute to the "degenerate embedding space" problems reported in later-stage models [5]. Our PAD metric operationalizes concept drift in a task-grounded way, distinguishing superficial representational change from semantically meaningful drift.

---

## 5. Conclusion

TokenShift provides a principled, multi-metric framework for characterizing LLM training dynamics, revealing consistent three-phase representational evolution that informs optimal checkpointing for continual learning and domain adaptation.

---

## Data Availability

Checkpoint embeddings and probing datasets: HuggingFace datasets `TokenShift/1.3B-checkpoints`. Code: https://github.com/FakeResearchOrg/TokenShift.

## References

[1] Raghu M et al. SVCCA: Singular vector canonical correlation analysis for deep learning dynamics. NeurIPS 2017.  
[2] Ke Z et al. Continual pre-training of language models. ICLR 2023.  
[3] Ethayarajh K. How contextual are contextualized word representations? EMNLP 2019.  
[4] Tenney I et al. BERT rediscovers the classical NLP pipeline. ACL 2019.  
[5] Gao T et al. SimCSE: Simple contrastive learning of sentence embeddings. EMNLP 2021.
