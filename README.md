# V-JEPA 2 Chest X-Ray Classification

> Fine-tuning V-JEPA 2 pretrained representations for chest X-ray classification (Normal vs Pneumonia detection).

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## About the Project

This research project applies **V-JEPA 2** (Meta AI / FAIR, 2025) — a state-of-the-art self-supervised model originally designed for video understanding — to **chest X-ray classification** for pneumonia detection.

### Research Motivation

- V-JEPA 2 has **never been benchmarked** in medical imaging domain
- Chest X-ray classification is a **clinically significant** problem
- No prior work has applied JEPA-based models to X-ray imaging

## Quick Start

```bash
# Clone the repository
git clone https://github.com/rezzz59/v-jepa-2-chest-xray.git
cd v-jepa-2-chest-xray

# Open notebooks in Google Colab or Jupyter
jupyter notebook notebooks/
```

## Project Structure

```
v-jepa-2-chest-xray/
├── notebooks/
│   ├── 01_setup_environment.ipynb    # Environment setup
│   └── 02_data_preparation.ipynb      # Data loading & preprocessing
├── GUIDES.md                          # Personal research notes
└── README.md                          # This file
```

## Dataset

**Kaggle Chest X-Ray Images (Pneumonia)**
- ~5,863 images (Normal + Pneumonia)
- Split: 70% training / 15% validation / 15% testing

> Download: [Kaggle Chest X-Ray Images Dataset](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia)

## Methods

### Phase 1 — Baseline: Linear Probe
Evaluate frozen V-JEPA 2 features with a linear classifier head.

### Phase 2 — Full Fine-Tuning
End-to-end fine-tuning of V-JEPA 2 for chest X-ray classification.

## Requirements

```bash
pip install torch torchvision timm pandas numpy scikit-learn matplotlib
```

- Python 3.10+
- PyTorch 2.0+
- timm (for V-JEPA 2 model)
- pandas, numpy, scikit-learn, matplotlib

## Research Timeline

| Phase | Description | Week |
|-------|-------------|------|
| 1 | Setup & Foundation | 1-2 |
| 2 | Linear Probe Baseline | 3-4 |
| 3 | Full Fine-Tune | 5-6 |
| 4 | Model Comparison | 7-8 |
| 5 | Analysis & Ablation | 9-10 |
| 6 | Paper Writing | 11-14 |
| 7 | Submission & Revision | 15+ |

## Target Publication

- **SINTA 2** or **Scopus-indexed Journal**

## References

- Assran et al., *"Joint-Embedding Predictive Architecture"*, Meta AI / FAIR, 2025
- Deng et al., *"Chest X-Ray Images (Pneumonia)"*, Kaggle

## License

This project is licensed under the MIT License.
