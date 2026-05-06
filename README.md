# Layer-Wise CNN Feature Extraction and SVM Classification for Ball-Bearing Fault Diagnosis

This repository contains the Python material used to support the study of a hybrid CNN-SVM model for ball-bearing fault diagnosis using vibration signals from the Case Western Reserve University (CWRU) Bearing Data Center.

The goal is to compare manual statistical-feature classification with automatic CNN-based feature extraction followed by SVM classification. The current version also includes a layer-wise ablation study, where SVM classifiers are trained on representations extracted from different CNN layers.

## References and data

- CWRU Bearing Data Center dataset: https://engineering.case.edu/bearingdatacenter/download-data-file
- Master thesis: https://doi.org/10.47749/T/UNICAMP.2024.1434821
- Paper: Loading

The CWRU data files are not included in this repository because they are external benchmark data. Download them from the official CWRU Bearing Data Center page and place the files in the dataset folder expected by the notebook/script.

## Repository contents

- `hybrid_cnn_svm_bearing_diagnosis.ipynb`: GitHub-friendly notebook for checking dependencies, locating the dataset, loading saved ablation outputs, and generating a compact results summary.
- `eai_ablation_experiments.py` and/or `eai_ablation_experiments.ipynb`: full experiment code for the computationally expensive layer-wise ablation, if included in the repository.

## Main workflow

1. Download the CWRU bearing data from the official link above.
2. Keep the dataset outside Git when possible, or document the local path used.
3. Run the notebook for a quick check of dependencies, paths, and saved outputs.
4. Run the full ablation script/notebook only when retraining is required.
5. Save generated CSV files and figures so the article results can be reproduced without rerunning every model.

## Expected Python packages

The main experiments use:

- `numpy`
- `pandas`
- `scipy`
- `scikit-learn`
- `matplotlib`
- `tensorflow`
- `jupyter`

For the full ablation experiment, a GPU or a reserved workstation/cluster is recommended.

## Important note

High accuracy on CWRU should be interpreted as controlled public-benchmark evidence, not as complete industrial validation. The thesis and article discuss known limitations of the CWRU benchmark and why automatic feature extraction is still useful for comparing diagnostic representations.
