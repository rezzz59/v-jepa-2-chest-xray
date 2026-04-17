# Research Design: V-JEPA 2 for Chest X-Ray Classification

**Date:** 2026-04-17
**Status:** Approved
**Topic:** Fine-tuning V-JEPA 2 Pretrained Representations for Chest X-Ray Classification: Normal vs Pneumonia Detection

---

## 1. Research Gap

- V-JEPA 2 (Meta AI / FAIR, 2025) adalah model self-supervised video state-of-the-art
- Belum ada yang mengaplikasikan V-JEPA 2 ke medical imaging domain
- Chest X-Ray classification (Normal vs Pneumonia) adalah masalah penting secara klinis
- Research gap: tidak ada benchmark V-JEPA 2 di Chest X-Ray

## 2. Proposed Approach

```
Step 1: Load pretrained V-JEPA 2 (ViT-L/16, ~300M params)
         dari facebookresearch/jepa

Step 2: Gunakan 2 strategi evaluasi:
         a) Linear Probe — freeze backbone, train hanya classifier head
         b) Full Fine-tune — unfreeze & train seluruh model

Step 3: Train & evaluate di Chest X-Ray (Normal vs Pneumonia)

Step 4: Bandingkan dengan baseline:
         - ResNet-50 (supervised)
         - V-JEPA 1 (linear probe)
         - Fully-supervised ViT
```

## 3. Dataset

**Kaggle Chest X-Ray Images (Pneumonia):**
- ~5,863 images (Normal + Pneumonia)
- Free download, tidak perlu izin etik
- Split: 70% train / 15% val / 15% test

## 4. Expected Contributions

1. First benchmark V-JEPA 2 di medical imaging domain
2. Empirical comparison: linear probe vs full fine-tune untuk pretrained JEPA
3. Insight: apakah video-pretrained features transfer ke medical images
4. Reference paper untuk researcher lain yang mau apply JEPA ke medical

## 5. Expected Results (Estimasi)

| Model | Expected Acc |
|---|---|
| V-JEPA 2 (linear probe) | ~75-85% |
| V-JEPA 2 (fine-tune) | ~88-93% |
| ResNet-50 (supervised) | ~85-90% |
| V-JEPA 1 (linear probe) | ~70-80% |

## 6. Timeline

| Fase | Aktivitas | Minggu |
|---|---|---|
| 1 | Persiapan & Fondasi | 1-2 |
| 2 | Baseline — Linear Probe | 3-4 |
| 3 | Full Fine-tune V-JEPA 2 | 5-6 |
| 4 | Perbandingan Model | 7-8 |
| 5 | Analisis & Ablation | 9-10 |
| 6 | Penulisan Paper | 11-14 |
| 7 | Submit & Revisi | 15+ |

**Total: ~4-5 bulan realistis**

## 7. Constraints & Conditions

- GPU: Colab (free tier, upgrade to Pro if needed)
- Skill: Familiar PyTorch, CNN basics; ViT/JEPA perlu dipelajari
- Target publication: SINTA 2 atau Scopus journal
- Dataset: Kaggle Chest X-Ray (easy to obtain)
