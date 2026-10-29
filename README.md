# Sugarcane Disease Explainability and Bioethanol Process Analysis

An academic Python project exploring explainable machine learning and chemical engineering through two independent modules.

## Part A — Sugarcane Leaf-Disease Classification

Classifies sugarcane leaf images into Healthy, Mosaic, RedRot, Rust, and Yellow categories using neural networks, including MobileNetV2. SHAP supports interpretation of model predictions.

The revised pipeline includes:

- Independent stratified training, validation, and test splits.
- Exact-duplicate removal.
- Corrected MobileNetV2 preprocessing.
- Early stopping.
- Training-data backgrounds for SHAP.

## Part B — Bioethanol Process Modelling

Models a simplified first-generation bioethanol process using an aqueous glucose-equivalent feed.

Features include:

- Stoichiometric balances for ethanol, CO₂, unconverted sugar, and recovery losses.
- Sensible-heating and ethanol-recovery heat estimates.
- Steam consumption, utility cost, and utility-emission estimates.
- Sensitivity analysis for feed composition, conversion, recovery heat, and heat recovery.
- Monte Carlo uncertainty propagation across 2,000 scenarios.
- Operating-point selection subject to vessel-capacity and minimum-production constraints.

## Execution Status

### Part B

Executed successfully, including material-balance, limiting-case, and constraint checks.

Under the illustrative base-case assumptions:

| Parameter | Value |
|---|---:|
| Feed flow rate | 1,000 kg/h |
| Recovered ethanol equivalent | 72.128 kg/h |
| Estimated steam requirement | 216.08 kg/h |

These results are model estimates based on assumed inputs, not measured plant performance.

### Part A

Reviewed and patched but not retrained or evaluated in this revision.

The image dataset and TensorFlow environment were unavailable, and pretrained weights were not supplied. No improved classification accuracy is claimed.

## Scope and Limitations

- Process results are assumption-based screening estimates, not experimentally validated plant predictions.
- The model does not include rigorous distillation, dehydration, complete energy balances, or a second-generation bagasse conversion process.
- Leaf-disease predictions are not used to infer ethanol yield.
- Connecting the modules requires paired image, feedstock-quality, and fermentation measurements.

## Technologies

- Python
- NumPy
- pandas
- TensorFlow/Keras
- scikit-learn
- SHAP
- Matplotlib
- Seaborn

## Acknowledgements

The original leaf-classification notebook credits:

- Nursultan Sheishekeyev
- Mateusz Zbigniew Zalewski
- Ferran Oliver Gerones

Their attribution is retained. Subsequent modifications and the process-analysis extension should be documented separately.
