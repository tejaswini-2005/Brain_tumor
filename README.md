# Radiomics XAI Dashboard for BraTS 2021

This project provides an end-to-end explainable AI dashboard for brain tumor segmentation quality assessment using radiomics features and SHAP explanations. It uses existing BraTS 2021 images, predicted segmentation masks, and radiomics CSV inputs.

Structure:
- `app.py` — Streamlit dashboard entrypoint
- `project/radiomics` — data loading and feature processing
- `project/metrics` — segmentation metrics
- `project/models` — training and model utilities
- `project/explainability` — SHAP utilities
- `project/visualization` — 3D visualization helpers
- `project/reports` — report generation
- `project/configs/config.yaml` — basic configuration
- `requirements.txt` — Python dependencies

Quick start:

1. Create a Python environment and install dependencies:

```bash
pip install -r requirements.txt
```

2. Update `project/configs/config.yaml` paths to point to your dataset and outputs.

3. Run the Streamlit app:

```bash
streamlit run app.py
```

Notes:
- This scaffold provides modular functions for data loading, metrics, feature processing, modeling, SHAP explanations, and interactive 3D visualization. It expects existing radiomics CSV and segmentation outputs.
- Use `project/models/train_model.py` to train and save a model, then restart the app to enable SHAP explanations.
