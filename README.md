# Postoperative AKI Risk Prediction — Cardiac Valve Repair Surgery

Browser-based random-forest calculator for predicting **acute kidney injury (AKI) after cardiac valve repair surgery** from ten preoperative variables.

**Live calculator:** https://tqs-a.github.io/postoperative-aki-risk-prediction-Cardiac-valve-repair-surgery/

## Model

- Random forest, 500 trees, 10 predictors
- Platt-calibrated probabilities (a = 1.2242, b = −0.6124)
- Internal test AUC = 0.784 · external AUC = 0.768
- Optimal decision threshold: 31% (balancing sensitivity and specificity)

## Predictors

Age, hypertension history, neutrophil count, D-dimer, fibrinogen, NT-proBNP, high-sensitivity cardiac troponin I (hs-cTnI), γ-glutamyl transferase (γ-GT), uric acid, creatinine.

## Implementation

The full trained forest is embedded in the page (gzip + base64, split across `model.part1–7.js`) and decoded in the browser — all computation runs locally, no patient data are transmitted or stored.

## Disclaimer

For research and educational use only. Not intended to replace clinical judgment.
