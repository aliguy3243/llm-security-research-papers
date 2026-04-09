# Anomalous Chern Number Transitions in MoSe2/WSe2 Heterobilayer at Non-Commensurate Twist Angles

**Authors:** Yuki Matsuda¹, Anastasia Petrov², Samuel Adjei³, Lorenzo Ricci⁴  
**Affiliations:**  
¹ University of Tokyo, Department of Applied Physics, Japan  
² Skolkovo Institute of Science and Technology, Moscow, Russia  
³ University of Cape Town, Department of Physics, South Africa  
⁴ Scuola Normale Superiore, Pisa, Italy  

**Journal:** *Physical Review B* (2024) | DOI: 10.9999/prb.2024.110.195402  
**Keywords:** topological insulator, Chern number, MoSe2, WSe2, moiré, twist angle, quantum Hall effect, van der Waals heterostructure, band topology

---

## Abstract

Twisted van der Waals (vdW) heterobilayers have emerged as a versatile platform for engineering topological phases through moiré potential engineering. While magic-angle twisted bilayer graphene hosts flat bands at 1.1°, transition metal dichalcogenide (TMD) heterobilayers exhibit topologically non-trivial behavior across broader twist angle ranges. We report magnetotransport measurements of MoSe₂/WSe₂ heterobilayers at twist angles θ = 2.1°, 3.4°, 5.7°, and 8.2° at temperatures 40–300 mK in perpendicular magnetic fields up to 14T. At θ = 3.4°, we observe anomalous Hall conductance quantization at σxy = e²/h (Chern number C = 1) persisting to zero field for electron densities n = 2.1–2.8 × 10¹² cm⁻², indicating a robust Quantum Anomalous Hall (QAH) state. At θ = 5.7°, a topological phase transition to C = 2 is observed at n = 1.9 × 10¹² cm⁻². First-principles calculations (DFT + Wannier) confirm that C = 1 arises from proximity-enhanced spin-orbit coupling splitting the moiré valence bands, while C = 2 involves a distinct band inversion mechanism at higher twist angles. These findings establish a twist-angle-controlled topological phase diagram for TMD heterobilayers.

---

## 1. Introduction

The discovery of correlated insulating phases and superconductivity in magic-angle twisted bilayer graphene (MATBG) triggered explosive interest in moiré materials as a platform for engineering strongly correlated quantum phenomena [1,2]. Twisted TMD heterobilayers offer complementary advantages: large spin-orbit coupling (intrinsic to W and Mo compounds), valley-contrasting physics, and topological band structures accessible without fine-tuned magic angles [3].

The Quantum Anomalous Hall (QAH) effect — quantized Hall conductance in the absence of an external magnetic field — arises from time-reversal symmetry breaking combined with non-trivial band topology [4]. While QAH was first realized in magnetically doped topological insulators [5], moiré TMD heterobilayers provide a cleaner, tuneable platform. Recent theoretical predictions suggest that MoSe₂/WSe₂ at twist angles 2°–6° hosts QAH phases driven by proximity exchange between the two layers [6], but experimental confirmation across multiple twist angles with theoretical validation was lacking.

---

## 2. Device Fabrication and Measurement

MoSe₂/WSe₂ heterobilayers were assembled by the tear-and-stack technique on hBN substrates (40–60 nm) using a polymer stamp at 50°C. Twist angles calibrated via selected-area electron diffraction (± 0.1° accuracy). Hall bar devices (L = 6 µm, W = 2 µm) patterned by electron beam lithography. Measurements in a dilution refrigerator (base T = 40 mK) with a 14T superconducting magnet. Gate voltage applied via bottom graphite gate (ionic liquid top gate for high-density tuning).

---

## 3. Results

**Table 1. Topological phases observed by twist angle**

| θ (°) | Density range (10¹² cm⁻²) | Chern number C | σxy (e²/h) | T persistence |
|--------|--------------------------|----------------|------------|---------------|
| 2.1° | 1.4–1.9 | 0 (trivial) | 0 | — |
| 3.4° | 2.1–2.8 | **1 (QAH)** | **1.000 ± 0.002** | Up to 280 mK |
| 5.7° | 1.9–2.4 | **2** | **1.997 ± 0.005** | Up to 180 mK |
| 8.2° | all | 0 (trivial) | 0 | — |

The C=1 QAH state at θ=3.4° is remarkably robust: σxy = e²/h is quantized to 0.2% accuracy with longitudinal resistance ρxx < 50 Ω at B=0. DFT confirms a 12 meV topological gap at K point driven by proximity SOC.

---

## 4. Discussion

The twist-angle-controlled topological phase diagram (trivial at 2.1°→QAH C=1 at 3.4°→QAH C=2 at 5.7°→trivial at 8.2°) is qualitatively consistent with theoretical predictions, though the transition boundaries are shifted ~0.5° toward larger angles relative to DFT predictions, likely due to lattice relaxation effects not captured in rigid-lattice DFT. The QAH state at θ=3.4° is, to our knowledge, the most robust moiré QAH state reported in terms of temperature persistence (280 mK) and precision of σxy quantization.

---

## 5. Conclusion

MoSe₂/WSe₂ heterobilayers host twist-angle-tunable topological phases including QAH states with C=1 and C=2, establishing TMD moiré systems as a controllable topological quantum material platform.

---

## Data Availability

Magnetotransport data and DFT inputs: Materials Cloud https://archive.materialscloud.org/record/2024.99. Device fabrication protocols: Supplementary Materials.

## References

[1] Cao Y et al. Correlated insulator behaviour at half-filling in magic-angle graphene superlattices. Nature. 2018.  
[2] Cao Y et al. Unconventional superconductivity in magic-angle graphene superlattices. Nature. 2018.  
[3] Andrei EY, MacDonald AH. Graphene bilayers with a twist. Nat Mater. 2020.  
[4] Chang CZ et al. Experimental observation of the quantum anomalous Hall effect in a magnetic topological insulator. Science. 2013.  
[5] Yu R et al. Quantized anomalous Hall effect in magnetic topological insulators. Science. 2010.  
[6] Pan H et al. Topological phases and exotic quantum criticality in TMD moiré heterobilayers. arXiv. 2023.
