# Edits Made to `param_card.dat`

This file explains the key modifications made to `param_card.dat` during MadGraph5 simulations for the scalar leptoquark Π₇ (also known as R₂) in the SMEFT framework.

>   We **do not upload the full param_card** here, because:
> - It is dynamically generated from the UFO model.
> - Most lines are untouched; only a few parameters are modified.

---

## MASS Block

*(Adjust the mass as per the benchmark point used in your run)*

---

## YUKAWA Couplings

Only `y_32` was turned ON for simulations (all others OFF):

This corresponds to enabling the third-generation quark to second-generation lepton transition only.

---

##  DECAY Width

Let MadGraph calculate the decay width automatically, or use an analytical value if needed.

---

##  Reasoning Behind Parameter Choices

This simulation setup aimed to isolate the collider signature of the scalar leptoquark Π₇ with minimal model assumptions:

- Only `y_32` was activated to **isolate its contribution** and avoid flavor interference
- All other couplings (`y_12`, `y_22`, etc.) were set to zero for clarity
- Mass `M_LQ = 1000 GeV` was selected as a benchmark to study cross-section exclusion limits
- Width left at zero so MadGraph calculates it automatically from allowed decays
- No decay branching ratios were hardcoded — to allow model flexibility

This setup formed the **baseline scenario** for collider analysis and was later extended with multiple benchmark points during parameter scans.

---

## How to Reproduce This Setup

1. Install and run MadGraph5
2. Import the `SLQ_UFO` model:



