# V-JEPA 2 for Chest X-Ray Classification

> **Fine-tuning V-JEPA 2 Pretrained Representations for Chest X-Ray Classification: Normal vs Pneumonia Detection**

## Overview

Penelitian ini bertujuan untuk mengaplikasikan **V-JEPA 2** (Meta AI / FAIR, 2025) — model self-supervised video state-of-the-art — ke **Chest X-Ray classification** (Normal vs Pneumonia).

## Research Gap

- V-JEPA 2 BELUM PERNAH di-benchmark di medical imaging domain
- Chest X-Ray classification = masalah penting secara klinis
- Belum ada yang mengaplikasikan JEPA ke X-ray

## Timeline

| Fase | Aktivitas | Minggu |
|---|---|---|
| 1 | Persiapan & Fondasi | 1-2 |
| 2 | Baseline — Linear Probe | 3-4 |
| 3 | Full Fine-tune V-JEPA 2 | 5-6 |
| 4 | Perbandingan Model | 7-8 |
| 5 | Analisis & Ablation | 9-10 |
| 6 | Penulisan Paper | 11-14 |
| 7 | Submit & Revisi | 15+ |

## Project Structure

```
.
├── docs/                   # Documentation
│   └── superpowers/
│       └── specs/          # Research design specs
├── data/                   # Dataset (Chest X-Ray)
├── notebooks/              # Colab notebooks
├── models/                 # Trained models
├── experiments/           # Experiment logs & results
├── results/               # Final results & figures
└── paper/                  # Paper draft & final
```

## Dataset

**Kaggle Chest X-Ray Images (Pneumonia)**
- ~5,863 images (Normal + Pneumonia)
- Split: 70% train / 15% val / 15% test

## Target

- **SINTA 2** atau **Scopus Journal**
- Expected contribution: First benchmark V-JEPA 2 di medical imaging

## Status

- [x] Research design approved
- [ ] Phase 1: Persiapan & Fondasi (in progress)
- [ ] Phase 2: Linear Probe Baseline
- [ ] Phase 3: Full Fine-tune
- [ ] Phase 4: Model Comparison
- [ ] Phase 5: Analysis & Ablation
- [ ] Phase 6: Write Paper
- [ ] Phase 7: Submit
